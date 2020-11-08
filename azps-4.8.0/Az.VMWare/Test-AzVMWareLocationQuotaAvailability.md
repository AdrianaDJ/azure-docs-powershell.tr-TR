---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
ms.openlocfilehash: 9cb677ff172c986f18c7c11c00e0f8d7e0bbf5bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267936"
---
# <span data-ttu-id="ed3e5-101">Test-AzVMWareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="ed3e5-101">Test-AzVMWareLocationQuotaAvailability</span></span>

## <span data-ttu-id="ed3e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed3e5-102">SYNOPSIS</span></span>
<span data-ttu-id="ed3e5-103">Bölgeye göre abonelik için dönüş kotası</span><span class="sxs-lookup"><span data-stu-id="ed3e5-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="ed3e5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed3e5-104">SYNTAX</span></span>

### <span data-ttu-id="ed3e5-105">Çek (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ed3e5-105">Check (Default)</span></span>
```
Test-AzVMWareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ed3e5-106">Checkviaıdentity</span><span class="sxs-lookup"><span data-stu-id="ed3e5-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationQuotaAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ed3e5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed3e5-107">DESCRIPTION</span></span>
<span data-ttu-id="ed3e5-108">Bölgeye göre abonelik için dönüş kotası</span><span class="sxs-lookup"><span data-stu-id="ed3e5-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="ed3e5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed3e5-109">EXAMPLES</span></span>

### <span data-ttu-id="ed3e5-110">Örnek 1: kota kullanılabilirliğini denetleme</span><span class="sxs-lookup"><span data-stu-id="ed3e5-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="ed3e5-111">Kota kullanılabilirliğini denetleme</span><span class="sxs-lookup"><span data-stu-id="ed3e5-111">Check quota availability</span></span>

## <span data-ttu-id="ed3e5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed3e5-112">PARAMETERS</span></span>

### <span data-ttu-id="ed3e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed3e5-113">-DefaultProfile</span></span>
<span data-ttu-id="ed3e5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed3e5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed3e5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed3e5-115">-InputObject</span></span>
<span data-ttu-id="ed3e5-116">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed3e5-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed3e5-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="ed3e5-117">-Location</span></span>
<span data-ttu-id="ed3e5-118">Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="ed3e5-118">Azure region</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3e5-119">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ed3e5-119">-SubscriptionId</span></span>
<span data-ttu-id="ed3e5-120">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ed3e5-120">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3e5-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="ed3e5-121">-Confirm</span></span>
<span data-ttu-id="ed3e5-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ed3e5-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3e5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed3e5-123">-WhatIf</span></span>
<span data-ttu-id="ed3e5-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed3e5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed3e5-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ed3e5-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3e5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed3e5-126">CommonParameters</span></span>
<span data-ttu-id="ed3e5-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed3e5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed3e5-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ed3e5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed3e5-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed3e5-129">INPUTS</span></span>

### <span data-ttu-id="ed3e5-130">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. ıvmwareıdentity</span><span class="sxs-lookup"><span data-stu-id="ed3e5-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="ed3e5-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed3e5-131">OUTPUTS</span></span>

### <span data-ttu-id="ed3e5-132">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. Api20200320. ıquota</span><span class="sxs-lookup"><span data-stu-id="ed3e5-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="ed3e5-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed3e5-133">NOTES</span></span>

<span data-ttu-id="ed3e5-134">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="ed3e5-134">ALIASES</span></span>

<span data-ttu-id="ed3e5-135">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="ed3e5-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ed3e5-136">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ed3e5-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ed3e5-137">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ed3e5-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ed3e5-138">INPUTOBJECT <IVMWareIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="ed3e5-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ed3e5-139">`[AuthorizationName <String>]`: Özel bulutta ExpressRoute devresi yetkilendirmesi adı</span><span class="sxs-lookup"><span data-stu-id="ed3e5-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="ed3e5-140">`[ClusterName <String>]`: Özel buluttaki kümenin adı</span><span class="sxs-lookup"><span data-stu-id="ed3e5-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="ed3e5-141">`[HcxEnterpriseSiteName <String>]`: Özel bulutta HCX kurumsal sitesinin adı</span><span class="sxs-lookup"><span data-stu-id="ed3e5-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="ed3e5-142">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="ed3e5-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ed3e5-143">`[Location <String>]`: Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="ed3e5-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="ed3e5-144">`[PrivateCloudName <String>]`: Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="ed3e5-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="ed3e5-145">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ed3e5-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ed3e5-146">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="ed3e5-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="ed3e5-147">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ed3e5-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="ed3e5-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed3e5-148">RELATED LINKS</span></span>

