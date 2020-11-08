---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277692"
---
# <span data-ttu-id="bf43b-101">Az. ManagedServices modülü</span><span class="sxs-lookup"><span data-stu-id="bf43b-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="bf43b-102">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf43b-102">Description</span></span>
<span data-ttu-id="bf43b-103">Bu özellik, yönetilen hizmet sağlayıcılarının (MSPs) müşterileri tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bf43b-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="bf43b-104">Müşteriler, bir MSP 'yi kendi aboneliğini veya kaynak gruplarını yönetebilmelerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="bf43b-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="bf43b-105">Ayrıca, müşteri erişim vermeye ek olarak, erişimi kaldırabilir veya varolan erişimi görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="bf43b-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="bf43b-106">MSPs, kendilerine aboneliğe erişim izni atayan müşterilerin listesini görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="bf43b-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="bf43b-107">Bu işlemde iki nesne vardır: msp kullanıcılarına verilen MSP ve rol tanımlarını tanımlayan bir kayıt tanımı.</span><span class="sxs-lookup"><span data-stu-id="bf43b-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="bf43b-108">MSP isteğe bağlı olarak, bir aboneliği tanımla bir aboneliği tanımlayan bir yönetilen hizmetler marketi kullanarak bu nesneyi tanımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="bf43b-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="bf43b-109">Az. ManagedServices cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="bf43b-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="bf43b-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="bf43b-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="bf43b-111">Belirli bir kayıt atamasını veya kayıt atamalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="bf43b-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="bf43b-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="bf43b-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="bf43b-113">Belirli bir kayıt tanımını veya kayıt tanımlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="bf43b-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="bf43b-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="bf43b-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="bf43b-115">Bir kayıt ataması oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="bf43b-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="bf43b-116">Yeni-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="bf43b-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="bf43b-117">Kayıt tanımı oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="bf43b-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="bf43b-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="bf43b-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="bf43b-119">Kayıt atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bf43b-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="bf43b-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="bf43b-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="bf43b-121">Kayıt tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bf43b-121">Removes a registration definition.</span></span>
