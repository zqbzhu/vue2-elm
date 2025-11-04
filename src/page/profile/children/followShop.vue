<template>
    <div class="follow_shop_page">
        <head-top go-back='true' :head-title="followShopTitle"></head-top>
        <section>
            <shop-list :shop-list-arr="followedShops"></shop-list>
        </section>
        <foot-guide></foot-guide>
    </div>
</template>

<script>
import headTop from 'src/components/header/head'
import footGuide from 'src/components/footer/footGuide'
import shopList from 'src/components/common/shoplist'

export default {
    data(){
        return {
            followShopTitle: '关注店铺',
            // 虚假数据，模拟关注的店铺列表
            followedShops: [
                {
                    id: 1,
                    name: '肯德基(人民广场店)',
                    image_path: 'shop1.jpg',
                    rating: 4.8,
                    recent_order_num: 1234,
                    delivery_mode: { text: '外卖' },
                    float_minimum_order_amount: 20,
                    piecewise_agent_fee: { tips: '配送费¥5' },
                    distance: '500m',
                    order_lead_time: '30分钟',
                    supports: [
                        { id: 1, icon_name: '保' },
                        { id: 2, icon_name: '准' }
                    ]
                },
                {
                    id: 2,
                    name: '麦当劳(淮海路店)',
                    image_path: 'shop2.jpg',
                    rating: 4.7,
                    recent_order_num: 987,
                    delivery_mode: { text: '外卖' },
                    float_minimum_order_amount: 15,
                    piecewise_agent_fee: { tips: '配送费¥4' },
                    distance: '800m',
                    order_lead_time: '25分钟',
                    supports: [
                        { id: 1, icon_name: '保' }
                    ]
                },
                {
                    id: 3,
                    name: '星巴克(陆家嘴店)',
                    image_path: 'shop3.jpg',
                    rating: 4.9,
                    recent_order_num: 1567,
                    delivery_mode: { text: '外卖' },
                    float_minimum_order_amount: 30,
                    piecewise_agent_fee: { tips: '免配送费' },
                    distance: '1.2km',
                    order_lead_time: '40分钟',
                    supports: [
                        { id: 1, icon_name: '保' },
                        { id: 2, icon_name: '准' },
                        { id: 3, icon_name: '票' }
                    ]
                }
            ]
        }
    },
    components: {
        headTop,
        footGuide,
        shopList
    }
}
</script>

<style lang="scss" scoped>
    .follow_shop_page {
        background-color: #f5f5f5;
        min-height: 100vh;
    }
</style>