<template>
    <div class="row why__intro">
	    <div class="ctr">

            <!-- intro -->
            <div class="row">
                <h2>{{ whyTitle }}</h2>
                <div class="flex">
                    <div class="row why__excerpt" v-html="whyExcerpt" />
                </div>
            </div>

        </div>
    </div>
</template>
<script>
export default {
  name: 'why',
  // props
  props: [
    // eslint-disable-next-line vue/require-prop-types
    'whyTitle',
    'whyExcerpt',
    'whyButtonTitle',
    'whyButtonUrl'
  ]
}
</script>

