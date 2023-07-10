// beforeCreate和created=>setup =>发送ajax请求直接在 setup中发送即可
// beforeMountmounted===> onBeforeMount / onMounted
// beforeUpdate和 updated===> onBeforeUpdate / onUpdate
// beforeDestroy 和 destroyed===> onBeforeUnmount / onUnmounted
const getList = async () => {
  const res = await axios('https://apipc-xiaotuxian-front.itheima.net/home/banner');
  console.log(res);
};
getList();
onBeforeMount(() => {
  console.log(1);
});
onMounted(() => {
  console.log(2);
});
