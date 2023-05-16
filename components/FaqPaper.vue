<template>
    <div class="row faqs">
        <div class="ctr">
            <div class="row">
                <span class="faqs__title">
                    Frequently Asked Questions
                </span>
	        </div>
            <div class="row">
                <div class="faqs__grid">
                    <ul>

                        <li>
                            <a href="#">
                                <div class="faqs__icon">
                                    <span>?</span>
                                </div>
                                <div class="faqs__question">
                                    <span class="faqs__question-title">
                                        A simple question about paper recycling.
                                    </span>
                                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin bibendum luctus felis, vitae suscipit dui porttitor in. </p>
                                </div>
                            </a>
                        </li>

                        <li>
                            <a href="#">
                                <div class="faqs__icon">
                                    <span>?</span>
                                </div>
                                <div class="faqs__question">
                                    <span class="faqs__question-title">
                                        A simple question about paper recycling.
                                    </span>
                                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin bibendum luctus felis, vitae suscipit dui porttitor in. </p>
                                </div>
                            </a>
                        </li>

                        <li>
                            <a href="#">
                                <div class="faqs__icon">
                                    <span>?</span>
                                </div>
                                <div class="faqs__question">
                                    <span class="faqs__question-title">
                                        A simple question about paper recycling.
                                    </span>
                                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin bibendum luctus felis, vitae suscipit dui porttitor in. </p>
                                </div>
                            </a>
                        </li>

                        <li>
                            <a href="#">
                                <div class="faqs__icon">
                                    <span>?</span>
                                </div>
                                <div class="faqs__question">
                                    <span class="faqs__question-title">
                                        A simple question about paper recycling.
                                    </span>
                                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin bibendum luctus felis, vitae suscipit dui porttitor in. </p>
                                </div>
                            </a>
                        </li>

                        <li>
                            <a href="#">
                                <div class="faqs__icon">
                                    <span>?</span>
                                </div>
                                <div class="faqs__question">
                                    <span class="faqs__question-title">
                                        A simple question about paper recycling.
                                    </span>
                                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin bibendum luctus felis, vitae suscipit dui porttitor in. </p>
                                </div>
                            </a>
                        </li>

                        <li>
                            <a href="#">
                                <div class="faqs__icon">
                                    <span>?</span>
                                </div>
                                <div class="faqs__question">
                                    <span class="faqs__question-title">
                                        A simple question about paper recycling.
                                    </span>
                                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin bibendum luctus felis, vitae suscipit dui porttitor in. </p>
                                </div>
                            </a>
                        </li>

                        <li>
                            <a href="#">
                                <div class="faqs__icon">
                                    <span>?</span>
                                </div>
                                <div class="faqs__question">
                                    <span class="faqs__question-title">
                                        A simple question about paper recycling.
                                    </span>
                                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin bibendum luctus felis, vitae suscipit dui porttitor in. </p>
                                </div>
                            </a>
                        </li>

                        <li>
                            <a href="#">
                                <div class="faqs__icon">
                                    <span>?</span>
                                </div>
                                <div class="faqs__question">
                                    <span class="faqs__question-title">
                                        A simple question about paper recycling.
                                    </span>
                                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin bibendum luctus felis, vitae suscipit dui porttitor in. </p>
                                </div>
                            </a>
                        </li>

                    </ul>
                </div>
            </div>
	    </div>
    </div>
</template>
<style>
.faqs {
    background: #f7f7f7;
    padding: 6rem 0 4rem 0;
}

.faqs__title,
.faqs__question-title {
  color: #146636;
  display: block;
  text-transform: uppercase;
  font-size: 1.6rem;
  margin: 0 0 4rem 0;
  font-weight: 600;
  font-family: "Montserrat", sans-serif;
}

.faqs__question-title {
  font-size: 1.2rem;
  margin: 0 0 1rem 0;
}

.faqs__grid ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

.faqs__grid li {
    margin: 0 0 2rem 0;
    box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px, rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;
}

.faqs__grid li a {
    background: #fff;
    color: #666;
    padding: 2rem;
    display: flex;
    justify-content: flex-start;
    text-decoration: none;
}

.faqs__grid li a p {
    line-height: 1.4;
}

.faqs__icon {
    width: 50px;
}

.faqs__icon span {
    background: #146636;
    color: #fff;
    border-radius: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 50px;
    width: 50px;
    font-size: 2rem;
    font-weight: 600;
}

.faqs__question {
    flex: 1;
    padding: 0 0 0 2rem;
}

/* 768 */
@media only screen and (min-width: 768px) {
    .faqs__grid ul {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
    }

    .faqs__grid li {
        width: calc(50% - 1rem);
    }
}
</style>
<script>
export default {
  name: 'faq-paper',
}
</script>

