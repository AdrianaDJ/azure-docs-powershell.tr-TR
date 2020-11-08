---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: ff1fc53d7fec9a56564bbf536469ea9f745f9265
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267752"
---
# <span data-ttu-id="a2294-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="a2294-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="a2294-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2294-102">SYNOPSIS</span></span>
<span data-ttu-id="a2294-103">Belirtilen abonelikte adanmış bir HSM oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="a2294-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="a2294-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2294-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a2294-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2294-105">DESCRIPTION</span></span>
<span data-ttu-id="a2294-106">Belirtilen abonelikte adanmış bir HSM oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="a2294-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="a2294-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2294-107">EXAMPLES</span></span>

### <span data-ttu-id="a2294-108">Örnek 1: var olan sanal ağda özel bir HSM oluşturma</span><span class="sxs-lookup"><span data-stu-id="a2294-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="a2294-109">Bu komut, var olan bir sanal ağda atanmış bir HSM oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a2294-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="a2294-110">**Not:** Şu anda, `New-AzDedicatedHsm` Azure 'DA HSM tam olarak sağlanmadan önce döndürdüğü bir sınırlama vardır.</span><span class="sxs-lookup"><span data-stu-id="a2294-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="a2294-111">Bu nedenle yeni bir HSM oluşturduktan sonra lütfen durumunu sorgulayın ve kullanmadan `Get-AzDedicatedHsm` önce olduğundan emin olun `Provisioning State` `Succeeded` .</span><span class="sxs-lookup"><span data-stu-id="a2294-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="a2294-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2294-112">PARAMETERS</span></span>

### <span data-ttu-id="a2294-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="a2294-113">-AsJob</span></span>
<span data-ttu-id="a2294-114">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="a2294-114">Run the command as a job</span></span>

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

### <span data-ttu-id="a2294-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2294-115">-DefaultProfile</span></span>
<span data-ttu-id="a2294-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a2294-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2294-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="a2294-117">-Location</span></span>
<span data-ttu-id="a2294-118">Adanmış HSM 'nin oluşturulması gereken desteklenen Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="a2294-118">The supported Azure location where the dedicated HSM should be created.</span></span>

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

### <span data-ttu-id="a2294-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a2294-119">-Name</span></span>
<span data-ttu-id="a2294-120">Adanmış HSM adı</span><span class="sxs-lookup"><span data-stu-id="a2294-120">Name of the dedicated Hsm</span></span>

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

### <span data-ttu-id="a2294-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a2294-121">-NetworkInterface</span></span>
<span data-ttu-id="a2294-122">Adanmış HSM ile ilişkili ağ arabirimlerinin kaynak kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2294-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="a2294-123">Oluşturmak için, NETWORKıNTERFACE özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a2294-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.INetworkInterface[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2294-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a2294-124">-NoWait</span></span>
<span data-ttu-id="a2294-125">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="a2294-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a2294-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2294-126">-ResourceGroupName</span></span>
<span data-ttu-id="a2294-127">Kaynağın ait olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a2294-127">The name of the Resource Group to which the resource belongs.</span></span>

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

### <span data-ttu-id="a2294-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="a2294-128">-Sku</span></span>
<span data-ttu-id="a2294-129">Adanmış HSM SKU 'SU</span><span class="sxs-lookup"><span data-stu-id="a2294-129">SKU of the dedicated HSM</span></span>

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

### <span data-ttu-id="a2294-130">-Stampıd</span><span class="sxs-lookup"><span data-stu-id="a2294-130">-StampId</span></span>
<span data-ttu-id="a2294-131">Bu alan, RP kullanılabilirlik bölgelerini desteklemiyorsa kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="a2294-131">This field will be used when RP does not support Availability zones.</span></span>

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

### <span data-ttu-id="a2294-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a2294-132">-SubnetId</span></span>
<span data-ttu-id="a2294-133">/Subscriptions/{subscriptionid}/ResourceGroups/{groupgroupname}/...</span><span class="sxs-lookup"><span data-stu-id="a2294-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

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

### <span data-ttu-id="a2294-134">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a2294-134">-SubscriptionId</span></span>
<span data-ttu-id="a2294-135">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="a2294-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a2294-136">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a2294-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a2294-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a2294-137">-Tag</span></span>
<span data-ttu-id="a2294-138">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="a2294-138">Resource tags</span></span>

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

### <span data-ttu-id="a2294-139">-Bölge</span><span class="sxs-lookup"><span data-stu-id="a2294-139">-Zone</span></span>
<span data-ttu-id="a2294-140">Adanmış HSM bölgeleri.</span><span class="sxs-lookup"><span data-stu-id="a2294-140">The Dedicated Hsm zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2294-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="a2294-141">-Confirm</span></span>
<span data-ttu-id="a2294-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a2294-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2294-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2294-143">-WhatIf</span></span>
<span data-ttu-id="a2294-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2294-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2294-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a2294-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2294-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2294-146">CommonParameters</span></span>
<span data-ttu-id="a2294-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2294-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2294-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a2294-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2294-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2294-149">INPUTS</span></span>

## <span data-ttu-id="a2294-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2294-150">OUTPUTS</span></span>

### <span data-ttu-id="a2294-151">Microsoft. Azure. PowerShell. cmdlet. ayrılmış Atedhsm. modeller. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="a2294-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="a2294-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2294-152">NOTES</span></span>

<span data-ttu-id="a2294-153">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="a2294-153">ALIASES</span></span>

<span data-ttu-id="a2294-154">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="a2294-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a2294-155">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a2294-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a2294-156">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a2294-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a2294-157">NETWORKINTERFACE <ınetworkınterface [] >: adanmış HSM ile ilişkili ağ arabirimlerinin kaynak kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2294-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="a2294-158">`[PrivateIPAddress <String>]`: Arabirimin özel IP adresi</span><span class="sxs-lookup"><span data-stu-id="a2294-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="a2294-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2294-159">RELATED LINKS</span></span>

