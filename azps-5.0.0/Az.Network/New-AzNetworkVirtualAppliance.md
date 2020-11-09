---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 9b3991a24430afa74853f742bffa12b772dbeaf2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323311"
---
# <span data-ttu-id="500f5-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="500f5-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="500f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="500f5-102">SYNOPSIS</span></span>
<span data-ttu-id="500f5-103">Ağ sanal bir gereç kaynağı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="500f5-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="500f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="500f5-104">SYNTAX</span></span>

### <span data-ttu-id="500f5-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="500f5-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="500f5-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="500f5-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="500f5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="500f5-107">DESCRIPTION</span></span>
<span data-ttu-id="500f5-108">New-AzNetworkVirtualAppliance komutu, Azure 'da bir ağ sanal gereç kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="500f5-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="500f5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="500f5-109">EXAMPLES</span></span>

### <span data-ttu-id="500f5-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="500f5-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="500f5-111">Kaynak grubunda yeni bir ağ sanal gereç kaynağı oluşturur: latestrg.</span><span class="sxs-lookup"><span data-stu-id="500f5-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="500f5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="500f5-112">PARAMETERS</span></span>

### <span data-ttu-id="500f5-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="500f5-113">-AsJob</span></span>
<span data-ttu-id="500f5-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="500f5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="500f5-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="500f5-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="500f5-116">Önyükleme yapılandırması blob URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="500f5-116">The Bootstrap configuration blob URL.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500f5-117">-Clouınıtconfiguration</span><span class="sxs-lookup"><span data-stu-id="500f5-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="500f5-118">Clouınıt yapılandırması düz metin olarak.</span><span class="sxs-lookup"><span data-stu-id="500f5-118">The Cloudinit configuration as plain text.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500f5-119">-Clouınıtconfigurationblob</span><span class="sxs-lookup"><span data-stu-id="500f5-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="500f5-120">Clouınıt yapılandırması BLOB depolama URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="500f5-120">The Cloudinit configuration blob storage URL.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500f5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500f5-121">-DefaultProfile</span></span>
<span data-ttu-id="500f5-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="500f5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="500f5-123">-Force</span><span class="sxs-lookup"><span data-stu-id="500f5-123">-Force</span></span>
<span data-ttu-id="500f5-124">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="500f5-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="500f5-125">-Kimlik</span><span class="sxs-lookup"><span data-stu-id="500f5-125">-Identity</span></span>
<span data-ttu-id="500f5-126">Yönetilen kimlik.</span><span class="sxs-lookup"><span data-stu-id="500f5-126">The Managed identity.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500f5-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="500f5-127">-Location</span></span>
<span data-ttu-id="500f5-128">Genel IP adresi konumu.</span><span class="sxs-lookup"><span data-stu-id="500f5-128">The public IP address location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500f5-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="500f5-129">-Name</span></span>
<span data-ttu-id="500f5-130">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="500f5-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500f5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="500f5-131">-ResourceGroupName</span></span>
<span data-ttu-id="500f5-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="500f5-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500f5-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="500f5-133">-ResourceId</span></span>
<span data-ttu-id="500f5-134">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="500f5-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500f5-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="500f5-135">-Sku</span></span>
<span data-ttu-id="500f5-136">Sanal Gereç SKU 'Su.</span><span class="sxs-lookup"><span data-stu-id="500f5-136">The Sku of the Virtual Appliance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500f5-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="500f5-137">-Tag</span></span>
<span data-ttu-id="500f5-138">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="500f5-138">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500f5-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="500f5-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="500f5-140">Sanal Gereç için ASN numarası.</span><span class="sxs-lookup"><span data-stu-id="500f5-140">The ASN number of the Virtual Appliance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500f5-141">-Virtualhubıd</span><span class="sxs-lookup"><span data-stu-id="500f5-141">-VirtualHubId</span></span>
<span data-ttu-id="500f5-142">Sanal hub 'ın kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="500f5-142">The Resource Id of the Virtual Hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500f5-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="500f5-143">-Confirm</span></span>
<span data-ttu-id="500f5-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="500f5-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="500f5-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="500f5-145">-WhatIf</span></span>
<span data-ttu-id="500f5-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="500f5-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="500f5-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="500f5-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="500f5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500f5-148">CommonParameters</span></span>
<span data-ttu-id="500f5-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="500f5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500f5-150">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="500f5-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500f5-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="500f5-151">INPUTS</span></span>

### <span data-ttu-id="500f5-152">System. String</span><span class="sxs-lookup"><span data-stu-id="500f5-152">System.String</span></span>

### <span data-ttu-id="500f5-153">Microsoft. Azure. Commands. Network. model. PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="500f5-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="500f5-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="500f5-154">System.Int32</span></span>

### <span data-ttu-id="500f5-155">Microsoft. Azure. Commands. Network. model. Psmanagedserviceıdentity</span><span class="sxs-lookup"><span data-stu-id="500f5-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="500f5-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="500f5-156">System.String[]</span></span>

### <span data-ttu-id="500f5-157">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="500f5-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="500f5-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="500f5-158">OUTPUTS</span></span>

### <span data-ttu-id="500f5-159">Microsoft. Azure. Commands. Network. model. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="500f5-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="500f5-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="500f5-160">NOTES</span></span>

## <span data-ttu-id="500f5-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="500f5-161">RELATED LINKS</span></span>
