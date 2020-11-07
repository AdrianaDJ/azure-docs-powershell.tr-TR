---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
ms.openlocfilehash: e10e60845c9aeb90b7c708a65f7d681d9894b022
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752854"
---
# <span data-ttu-id="2930d-101">New-AzHost</span><span class="sxs-lookup"><span data-stu-id="2930d-101">New-AzHost</span></span>

## <span data-ttu-id="2930d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2930d-102">SYNOPSIS</span></span>
<span data-ttu-id="2930d-103">Konak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2930d-103">Creates a  host.</span></span>

## <span data-ttu-id="2930d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2930d-104">SYNTAX</span></span>

```
New-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-Location] <String>
 -Sku <String> [-PlatformFaultDomain <Int32>] [-AutoReplaceOnFailure <Boolean>]
 [-LicenseType <DedicatedHostLicenseTypes>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2930d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2930d-105">DESCRIPTION</span></span>
<span data-ttu-id="2930d-106">Bu cmdlet bir konak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2930d-106">This cmdlet will create a Host.</span></span>

## <span data-ttu-id="2930d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2930d-107">EXAMPLES</span></span>

### <span data-ttu-id="2930d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2930d-108">Example 1</span></span>
```
PS C:\> New-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -Location $location -Sku $skuName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 0
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
ProvisioningTime     : 7/25/2019 8:34:16 PM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="2930d-109">Bu komut, verilen konak grubunda ve verilen konumda verilen SKU 'nun bir konağını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2930d-109">This command creates a host of the given Sku in the given host group and the given location.</span></span>

## <span data-ttu-id="2930d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2930d-110">PARAMETERS</span></span>

### <span data-ttu-id="2930d-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="2930d-111">-AsJob</span></span>
<span data-ttu-id="2930d-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2930d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2930d-113">-Autoreplacenfailure</span><span class="sxs-lookup"><span data-stu-id="2930d-113">-AutoReplaceOnFailure</span></span>
<span data-ttu-id="2930d-114">Bir başarısızlık durumunda konağın otomatik olarak değiştirilip değiştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2930d-114">Specifies whether the host should be replaced automatically in case of a failure.</span></span> <span data-ttu-id="2930d-115">Değer sağlanmadıysa ' true ' olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="2930d-115">The value is defaulted to 'true' when not provided.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2930d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2930d-116">-DefaultProfile</span></span>
<span data-ttu-id="2930d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2930d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2930d-118">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="2930d-118">-HostGroupName</span></span>
<span data-ttu-id="2930d-119">Konak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2930d-119">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2930d-120">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2930d-120">-LicenseType</span></span>
<span data-ttu-id="2930d-121">Konakta dağıtılan VM 'lere uygulanacak yazılım lisansı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2930d-121">Specifies the software license type that will be applied to the VMs deployed on the host.</span></span> <span data-ttu-id="2930d-122">Olası değerler: None, Windows_Server_Hybrid ve Windows_Server_Perpetual.</span><span class="sxs-lookup"><span data-stu-id="2930d-122">Possible values are: None, Windows_Server_Hybrid, and Windows_Server_Perpetual.</span></span>  <span data-ttu-id="2930d-123">Varsayılan değer yok 'Tur.</span><span class="sxs-lookup"><span data-stu-id="2930d-123">Default value is None.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.DedicatedHostLicenseTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, WindowsServerHybrid, WindowsServerPerpetual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2930d-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="2930d-124">-Location</span></span>
<span data-ttu-id="2930d-125">Konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2930d-125">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2930d-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="2930d-126">-Name</span></span>
<span data-ttu-id="2930d-127">Konağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2930d-127">Specifies the name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2930d-128">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="2930d-128">-PlatformFaultDomain</span></span>
<span data-ttu-id="2930d-129">Konağın platform hatası etki alanı sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2930d-129">Specifies the number of platform fault domain of the host.</span></span>  <span data-ttu-id="2930d-130">En küçük değer 0 ve en büyük değer 2 ' dir.</span><span class="sxs-lookup"><span data-stu-id="2930d-130">Then minimum value is 0 and the maximum value is 2.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2930d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2930d-131">-ResourceGroupName</span></span>
<span data-ttu-id="2930d-132">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2930d-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2930d-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="2930d-133">-Sku</span></span>
<span data-ttu-id="2930d-134">SKU 'nun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2930d-134">Specifies the name of the SKU.</span></span>

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

### <span data-ttu-id="2930d-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2930d-135">-Tag</span></span>
<span data-ttu-id="2930d-136">Etiketleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="2930d-136">Specifies Tags.</span></span>

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

### <span data-ttu-id="2930d-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="2930d-137">-Confirm</span></span>
<span data-ttu-id="2930d-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2930d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2930d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2930d-139">-WhatIf</span></span>
<span data-ttu-id="2930d-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2930d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2930d-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2930d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2930d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2930d-142">CommonParameters</span></span>
<span data-ttu-id="2930d-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2930d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2930d-144">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2930d-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2930d-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2930d-145">INPUTS</span></span>

### <span data-ttu-id="2930d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2930d-146">System.String</span></span>

## <span data-ttu-id="2930d-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2930d-147">OUTPUTS</span></span>

### <span data-ttu-id="2930d-148">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSHost</span><span class="sxs-lookup"><span data-stu-id="2930d-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="2930d-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2930d-149">NOTES</span></span>

## <span data-ttu-id="2930d-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2930d-150">RELATED LINKS</span></span>
