---
Module Name: Az.ManagedServices
Module Guid: d2a8f744-8dcb-4a13-ba80-eb181ff365ad
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.1
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 41d7b3afa19de95b677ff5db18ca38294b8559af
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/15/2019
ms.locfileid: "93751066"
---
# <span data-ttu-id="d7ecc-101">Az. ManagedServices modülü</span><span class="sxs-lookup"><span data-stu-id="d7ecc-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="d7ecc-102">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7ecc-102">Description</span></span>
<span data-ttu-id="d7ecc-103">Bu özellik, yönetilen hizmet sağlayıcılarının (MSPs) müşterileri tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d7ecc-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="d7ecc-104">Müşteriler, bir MSP 'yi kendi aboneliğini yönetebilmelerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="d7ecc-104">Customers give an MSP the ability to manage their subscription.</span></span> <span data-ttu-id="d7ecc-105">Ayrıca, müşteri erişim vermeye ek olarak, erişimi kaldırabilir veya mevcut erişim temsilcilerini görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="d7ecc-105">In addition to granting access, the customer can also remove access or view existing access delegations.</span></span> <span data-ttu-id="d7ecc-106">MSPs, kendilerine aboneliğe erişim izni atayan müşterilerin listesini görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="d7ecc-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="d7ecc-107">Bu işlemde iki nesne vardır: msp ve MSP 'yi tanımlayan bir kayıt tanımı.</span><span class="sxs-lookup"><span data-stu-id="d7ecc-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP.</span></span> <span data-ttu-id="d7ecc-108">MSP isteğe bağlı olarak, bir aboneliği tanımla bir aboneliği tanımlayan bir yönetilen hizmetler marketi kullanarak bu nesneyi tanımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="d7ecc-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="d7ecc-109">Az. ManagedServices cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="d7ecc-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="d7ecc-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d7ecc-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="d7ecc-111">Kayıt atamalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="d7ecc-111">Gets a list of the registration assignments.</span></span>

### [<span data-ttu-id="d7ecc-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d7ecc-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="d7ecc-113">Kayıt tanımlarının bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="d7ecc-113">Gets a list of the registration definitions.</span></span>

### [<span data-ttu-id="d7ecc-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d7ecc-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="d7ecc-115">Kayıt ataması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7ecc-115">Creates a registration assignment.</span></span>

### [<span data-ttu-id="d7ecc-116">Yeni-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d7ecc-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="d7ecc-117">Kayıt tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7ecc-117">Creates a registration definition.</span></span>

### [<span data-ttu-id="d7ecc-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d7ecc-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="d7ecc-119">Kayıt atamasını siler.</span><span class="sxs-lookup"><span data-stu-id="d7ecc-119">Deletes the registration assignment.</span></span>

### [<span data-ttu-id="d7ecc-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d7ecc-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="d7ecc-121">Kayıt tanımını siler.</span><span class="sxs-lookup"><span data-stu-id="d7ecc-121">Deletes the registration definition.</span></span>

