---
Module Name: AzureRM.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: ''
Help Version: 0.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
ms.openlocfilehash: bbbdd28f0ea3916581c20cf8f078eca1cb2ddca6
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93570862"
---
# <span data-ttu-id="b54fd-101">AzureRM. Pazar Placesıralanırken modülü</span><span class="sxs-lookup"><span data-stu-id="b54fd-101">AzureRM.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="b54fd-102">Tanım</span><span class="sxs-lookup"><span data-stu-id="b54fd-102">Description</span></span>
<span data-ttu-id="b54fd-103">Bu bölümdeki konular, Azure Resource Manager (ARM) çerçevesindeki Azure</span><span class="sxs-lookup"><span data-stu-id="b54fd-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="b54fd-104">Cmdlet 'ler Microsoft. Azure. Commands. Marketplacesıralanırken ad alanında bulunur.</span><span class="sxs-lookup"><span data-stu-id="b54fd-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="b54fd-105">Bu cmdlet 'ler, Azure kullanıcılarının bu çözümler için programlı dağıtıma olanak sağlayan bir Pazaryeri yasal koşullarını kabul etmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="b54fd-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="b54fd-106">Kullanıcılar halen kabul edilmiş yasal şartlar kümesini de reddedebilir.</span><span class="sxs-lookup"><span data-stu-id="b54fd-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="b54fd-107">AzureRM. Pazar Placesıralanırken cmdlet 'Ler</span><span class="sxs-lookup"><span data-stu-id="b54fd-107">AzureRM.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="b54fd-108">Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="b54fd-108">Get-AzureRmMarketplaceTerms</span></span>](Get-AzureRmMarketplaceTerms.md)
<span data-ttu-id="b54fd-109">Belirli bir yayıncı kimliği (yayımcı), teklif kimliği (ürün) ve plan kimliği (adı) için anlaşma şartlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="b54fd-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="b54fd-110">Bu komut tarafından döndürülen terimler nesnesinin yasal şartları kabul etmesi için Set-AzureRmMarketplaceTerms geçirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="b54fd-110">The terms object which is returned by this command should be passed to Set-AzureRmMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="b54fd-111">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="b54fd-111">Set-AzureRmMarketplaceTerms</span></span>](Set-AzureRmMarketplaceTerms.md)
<span data-ttu-id="b54fd-112">Verilen Yayımcı kimliği (yayımcı), teklif kimliği (ürün) ve plan kimliği (adı) için koşulları kabul edin veya reddedin.</span><span class="sxs-lookup"><span data-stu-id="b54fd-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="b54fd-113">Sözleşme şartlarını almak için lütfen Get-AzureRmMarketplaceTerms kullanın.</span><span class="sxs-lookup"><span data-stu-id="b54fd-113">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

