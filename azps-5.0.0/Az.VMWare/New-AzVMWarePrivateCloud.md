---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
ms.openlocfilehash: 5dd91db9a8141bf9992da9eb364b00301036a898
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323500"
---
# <span data-ttu-id="b6943-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="b6943-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="b6943-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6943-102">SYNOPSIS</span></span>
<span data-ttu-id="b6943-103">Özel bir bulut oluşturma veya güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b6943-103">Create or update a private cloud</span></span>

## <span data-ttu-id="b6943-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6943-104">SYNTAX</span></span>

```
New-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b6943-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6943-105">DESCRIPTION</span></span>
<span data-ttu-id="b6943-106">Özel bir bulut oluşturma veya güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b6943-106">Create or update a private cloud</span></span>

## <span data-ttu-id="b6943-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6943-107">EXAMPLES</span></span>

### <span data-ttu-id="b6943-108">Örnek 1: özel bulut oluşturma</span><span class="sxs-lookup"><span data-stu-id="b6943-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="b6943-109">Özel bulut oluşturma</span><span class="sxs-lookup"><span data-stu-id="b6943-109">Create private cloud</span></span>

## <span data-ttu-id="b6943-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6943-110">PARAMETERS</span></span>

### <span data-ttu-id="b6943-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="b6943-111">-AsJob</span></span>
<span data-ttu-id="b6943-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="b6943-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6943-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6943-113">-DefaultProfile</span></span>
<span data-ttu-id="b6943-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b6943-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6943-115">-Internet</span><span class="sxs-lookup"><span data-stu-id="b6943-115">-Internet</span></span>
<span data-ttu-id="b6943-116">İnternet bağlantısı etkinleştirildi veya devre dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="b6943-116">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6943-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="b6943-117">-Location</span></span>
<span data-ttu-id="b6943-118">Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="b6943-118">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6943-119">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="b6943-119">-ManagementClusterSize</span></span>
<span data-ttu-id="b6943-120">Küme boyutu</span><span class="sxs-lookup"><span data-stu-id="b6943-120">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6943-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="b6943-121">-Name</span></span>
<span data-ttu-id="b6943-122">Özel bulutun adı</span><span class="sxs-lookup"><span data-stu-id="b6943-122">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6943-123">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="b6943-123">-NetworkBlock</span></span>
<span data-ttu-id="b6943-124">Adres bloğunun aboneliğinizdeki VNet genelinde yanı sıra şirket içi olarak benzersiz olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b6943-124">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="b6943-125">CıDR biçiminin, A, B, C, D, 0 ile 255 arasındaki, B, C, D, 0 ile 22 arasındaki bir</span><span class="sxs-lookup"><span data-stu-id="b6943-125">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6943-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b6943-126">-NoWait</span></span>
<span data-ttu-id="b6943-127">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="b6943-127">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6943-128">-Nsxtparola</span><span class="sxs-lookup"><span data-stu-id="b6943-128">-NsxtPassword</span></span>
<span data-ttu-id="b6943-129">İsteğe bağlı olarak, özel bulut oluşturulduğunda NSX-T Yöneticisi parolasını ayarlama</span><span class="sxs-lookup"><span data-stu-id="b6943-129">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6943-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6943-130">-ResourceGroupName</span></span>
<span data-ttu-id="b6943-131">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b6943-131">The name of the resource group.</span></span>
<span data-ttu-id="b6943-132">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="b6943-132">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6943-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="b6943-133">-Sku</span></span>
<span data-ttu-id="b6943-134">SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="b6943-134">The name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6943-135">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b6943-135">-SubscriptionId</span></span>
<span data-ttu-id="b6943-136">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b6943-136">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6943-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b6943-137">-Tag</span></span>
<span data-ttu-id="b6943-138">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="b6943-138">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6943-139">-Vcenterparola</span><span class="sxs-lookup"><span data-stu-id="b6943-139">-VcenterPassword</span></span>
<span data-ttu-id="b6943-140">İsteğe bağlı olarak, özel bulut oluşturulduğunda vCenter Yöneticisi parolasını ayarlama</span><span class="sxs-lookup"><span data-stu-id="b6943-140">Optionally, set the vCenter admin password when the private cloud is created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6943-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="b6943-141">-Confirm</span></span>
<span data-ttu-id="b6943-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b6943-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6943-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6943-143">-WhatIf</span></span>
<span data-ttu-id="b6943-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b6943-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6943-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b6943-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6943-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6943-146">CommonParameters</span></span>
<span data-ttu-id="b6943-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6943-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6943-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b6943-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6943-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6943-149">INPUTS</span></span>

## <span data-ttu-id="b6943-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6943-150">OUTPUTS</span></span>

### <span data-ttu-id="b6943-151">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="b6943-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="b6943-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6943-152">NOTES</span></span>

<span data-ttu-id="b6943-153">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="b6943-153">ALIASES</span></span>

## <span data-ttu-id="b6943-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6943-154">RELATED LINKS</span></span>

