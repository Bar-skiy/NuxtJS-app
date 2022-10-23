<template>
    <h4 class="text-secondary">Users with id {{$route.params.id}}</h4>
</template>

<script>
export default {
    validate({params}) {
return /^[1, 2, 3, 4, 5]+$/.test(params.id)
    }
}
</script>