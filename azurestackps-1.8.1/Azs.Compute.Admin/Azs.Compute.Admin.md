---
Module Name: Azs.Compute.Admin
Module Guid: e662cef1-a477-40a2-ab9f-06e8de7cc423
Download Help Link:
  '[object Object]': 
Help Version:
  '[object Object]': 
Locale: en-US
ms.openlocfilehash: 8b74dd57a85a39403f56840dd0fc54b3f25184f1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935017"
---
# <span data-ttu-id="d0697-101">AZS. COMPUTE. Admin modülü</span><span class="sxs-lookup"><span data-stu-id="d0697-101">Azs.Compute.Admin Module</span></span>
## <span data-ttu-id="d0697-102">Tanım</span><span class="sxs-lookup"><span data-stu-id="d0697-102">Description</span></span>
<span data-ttu-id="d0697-103">İşlemi yeniden dengelenecek yönetilen disk geçiş işlerinin yanı sıra, işlem kotalarını, platform görüntülerini ve sanal makine uzantılarını yönetmeye yönelik işlevsellik sağlayan AzureStack COMPUTE yönetim modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="d0697-103">Preview release of the AzureStack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions, as well as managed disks migration jobs to rebalance storage.</span></span>

## <span data-ttu-id="d0697-104">AZS. COMPUTE. admin cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="d0697-104">Azs.Compute.Admin Cmdlets</span></span>
### [<span data-ttu-id="d0697-105">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="d0697-105">Add-AzsPlatformImage</span></span>](Add-AzsPlatformImage.md)
<span data-ttu-id="d0697-106">Belirli bir görüntü yapılandırmasından sanal makine platformu resmi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d0697-106">Add a virtual machine platform image from a given image configuration.</span></span>

### [<span data-ttu-id="d0697-107">Add-Azsvmexgeri</span><span class="sxs-lookup"><span data-stu-id="d0697-107">Add-AzsVMExtension</span></span>](Add-AzsVMExtension.md)
<span data-ttu-id="d0697-108">Yeni bir sanal makine uzantısı görüntüsü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d0697-108">Create a new virtual machine extension image.</span></span>

### [<span data-ttu-id="d0697-109">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="d0697-109">Get-AzsComputeQuota</span></span>](Get-AzsComputeQuota.md)
<span data-ttu-id="d0697-110">İşlem nesnelerinin kota sınırlarını belirten kotalar döndürür.</span><span class="sxs-lookup"><span data-stu-id="d0697-110">Returns quotas specifying the quota limits for compute objects.</span></span>

### [<span data-ttu-id="d0697-111">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="d0697-111">Get-AzsDisk</span></span>](Get-AzsDisk.md)
<span data-ttu-id="d0697-112">Belirtilen paylaşıma geçirilebileceğiniz yönetilen disklerin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d0697-112">Returns the list of managed disks which can be migrated in the specified share.</span></span>

### [<span data-ttu-id="d0697-113">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="d0697-113">Get-AzsDiskMigrationJob</span></span>](Get-AzsDiskMigrationJob.md)
<span data-ttu-id="d0697-114">Yönetilen disk geçiş işlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d0697-114">Returns the list of managed disk migration jobs.</span></span>

### [<span data-ttu-id="d0697-115">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="d0697-115">Get-AzsPlatformImage</span></span>](Get-AzsPlatformImage.md)
<span data-ttu-id="d0697-116">Platform görüntü deposuna yüklenen sanal makine resimlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d0697-116">Returns virtual machine images loaded into the platform image repository.</span></span>

### [<span data-ttu-id="d0697-117">Get-Azsvmexgeri</span><span class="sxs-lookup"><span data-stu-id="d0697-117">Get-AzsVMExtension</span></span>](Get-AzsVMExtension.md)
<span data-ttu-id="d0697-118">Şu anda kullanılabilen sanal makine görüntü uzantılarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="d0697-118">Returns virtual machine image extensions currently available.</span></span>

### [<span data-ttu-id="d0697-119">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="d0697-119">New-AzsComputeQuota</span></span>](New-AzsComputeQuota.md)
<span data-ttu-id="d0697-120">Hesaplama kaynaklarını sınırlandırmak için kullanılan yeni bir işlem kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d0697-120">Create a new compute quota used to limit compute resources.</span></span>

### [<span data-ttu-id="d0697-121">Yeni-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="d0697-121">New-AzsDiskMigrationJob</span></span>](New-AzsDiskMigrationJob.md)
<span data-ttu-id="d0697-122">Yönetilen diskleri belirtilen hedef paylaşıma geçirmek için yönetilen disk geçiş işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="d0697-122">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

### [<span data-ttu-id="d0697-123">Yeni-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="d0697-123">New-DataDiskObject</span></span>](New-DataDiskObject.md)
<span data-ttu-id="d0697-124">Yeni bir sanal makine platformu görüntüsü oluşturmak için kullanılan bir veri diski oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d0697-124">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

### [<span data-ttu-id="d0697-125">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="d0697-125">Remove-AzsComputeQuota</span></span>](Remove-AzsComputeQuota.md)
<span data-ttu-id="d0697-126">Belirtilen işlem kotasını siler.</span><span class="sxs-lookup"><span data-stu-id="d0697-126">Deletes specified compute quota.</span></span>

### [<span data-ttu-id="d0697-127">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="d0697-127">Remove-AzsPlatformImage</span></span>](Remove-AzsPlatformImage.md)
<span data-ttu-id="d0697-128">Platform görüntü deposundaki sanal makine yansımasını silin.</span><span class="sxs-lookup"><span data-stu-id="d0697-128">Delete a virtual machine image from the platform image repository.</span></span>

### [<span data-ttu-id="d0697-129">Remove-Azsvmexgeri</span><span class="sxs-lookup"><span data-stu-id="d0697-129">Remove-AzsVMExtension</span></span>](Remove-AzsVMExtension.md)
<span data-ttu-id="d0697-130">Sanal makine uzantısı görüntüsünü siler.</span><span class="sxs-lookup"><span data-stu-id="d0697-130">Deletes a virtual machine extension image.</span></span>

### [<span data-ttu-id="d0697-131">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="d0697-131">Set-AzsComputeQuota</span></span>](Set-AzsComputeQuota.md)
<span data-ttu-id="d0697-132">Sağlanan parametreleri kullanarak var olan bir işlem kotasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="d0697-132">Update an existing compute quota using the provided parameters.</span></span>

### [<span data-ttu-id="d0697-133">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="d0697-133">Stop-AzsDiskMigrationJob</span></span>](Stop-AzsDiskMigrationJob.md)
<span data-ttu-id="d0697-134">Yönetilen disk geçiş işini iptal etme.</span><span class="sxs-lookup"><span data-stu-id="d0697-134">Cancel a managed disk migration job.</span></span>

