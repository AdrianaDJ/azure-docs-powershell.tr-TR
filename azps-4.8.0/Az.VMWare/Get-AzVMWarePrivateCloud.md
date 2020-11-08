---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
ms.openlocfilehash: 31400d3b9b6e57190a852ae579fffcaa9fc60401
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268917"
---
# <span data-ttu-id="7651f-101">Get-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="7651f-101">Get-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="7651f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7651f-102">SYNOPSIS</span></span>
<span data-ttu-id="7651f-103">Özel bir bulut alın</span><span class="sxs-lookup"><span data-stu-id="7651f-103">Get a private cloud</span></span>

## <span data-ttu-id="7651f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7651f-104">SYNTAX</span></span>

### <span data-ttu-id="7651f-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7651f-105">List1 (Default)</span></span>
```
Get-AzVMWarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7651f-106">Al</span><span class="sxs-lookup"><span data-stu-id="7651f-106">Get</span></span>
```
Get-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7651f-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="7651f-107">GetViaIdentity</span></span>
```
Get-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7651f-108">Listeniz</span><span class="sxs-lookup"><span data-stu-id="7651f-108">List</span></span>
```
Get-AzVMWarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7651f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="7651f-109">DESCRIPTION</span></span>
<span data-ttu-id="7651f-110">Özel bir bulut alın</span><span class="sxs-lookup"><span data-stu-id="7651f-110">Get a private cloud</span></span>

## <span data-ttu-id="7651f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7651f-111">EXAMPLES</span></span>

### <span data-ttu-id="7651f-112">Örnek 1: abonelik altında özel bulutu Listele</span><span class="sxs-lookup"><span data-stu-id="7651f-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="7651f-113">Abonelik altında özel bulutu Listele</span><span class="sxs-lookup"><span data-stu-id="7651f-113">List private cloud under subscription</span></span>

### <span data-ttu-id="7651f-114">Örnek 2: kaynak grubu altında özel bulutu Listele</span><span class="sxs-lookup"><span data-stu-id="7651f-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="7651f-115">Kaynak grubu altında özel bulutu Listele</span><span class="sxs-lookup"><span data-stu-id="7651f-115">List private cloud under resource group</span></span>

### <span data-ttu-id="7651f-116">Örnek 3: özel bulut alın</span><span class="sxs-lookup"><span data-stu-id="7651f-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="7651f-117">Özel bulut alın</span><span class="sxs-lookup"><span data-stu-id="7651f-117">Get private cloud</span></span>

## <span data-ttu-id="7651f-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7651f-118">PARAMETERS</span></span>

### <span data-ttu-id="7651f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7651f-119">-DefaultProfile</span></span>
<span data-ttu-id="7651f-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7651f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7651f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7651f-121">-InputObject</span></span>
<span data-ttu-id="7651f-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7651f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7651f-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="7651f-123">-Name</span></span>
<span data-ttu-id="7651f-124">Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="7651f-124">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7651f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7651f-125">-ResourceGroupName</span></span>
<span data-ttu-id="7651f-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7651f-126">The name of the resource group.</span></span>
<span data-ttu-id="7651f-127">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="7651f-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7651f-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="7651f-128">-SubscriptionId</span></span>
<span data-ttu-id="7651f-129">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7651f-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7651f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7651f-130">CommonParameters</span></span>
<span data-ttu-id="7651f-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7651f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7651f-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7651f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7651f-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7651f-133">INPUTS</span></span>

### <span data-ttu-id="7651f-134">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. ıvmwareıdentity</span><span class="sxs-lookup"><span data-stu-id="7651f-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="7651f-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7651f-135">OUTPUTS</span></span>

### <span data-ttu-id="7651f-136">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="7651f-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="7651f-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7651f-137">NOTES</span></span>

<span data-ttu-id="7651f-138">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="7651f-138">ALIASES</span></span>

<span data-ttu-id="7651f-139">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="7651f-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7651f-140">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7651f-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7651f-141">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7651f-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7651f-142">INPUTOBJECT <IVMWareIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="7651f-142">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7651f-143">`[AuthorizationName <String>]`: Özel bulutta ExpressRoute devresi yetkilendirmesi adı</span><span class="sxs-lookup"><span data-stu-id="7651f-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="7651f-144">`[ClusterName <String>]`: Özel buluttaki kümenin adı</span><span class="sxs-lookup"><span data-stu-id="7651f-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="7651f-145">`[HcxEnterpriseSiteName <String>]`: Özel bulutta HCX kurumsal sitesinin adı</span><span class="sxs-lookup"><span data-stu-id="7651f-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="7651f-146">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="7651f-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7651f-147">`[Location <String>]`: Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="7651f-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="7651f-148">`[PrivateCloudName <String>]`: Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="7651f-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="7651f-149">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7651f-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7651f-150">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="7651f-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="7651f-151">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7651f-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="7651f-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7651f-152">RELATED LINKS</span></span>

