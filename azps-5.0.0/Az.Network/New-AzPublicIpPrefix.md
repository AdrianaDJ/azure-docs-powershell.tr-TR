---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: cc00afb5dcdd4cc11c61cf96f2ae8ac3bb201bb5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275973"
---
# <span data-ttu-id="af675-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="af675-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="af675-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af675-102">SYNOPSIS</span></span>
<span data-ttu-id="af675-103">Genel bir IP öneki oluşturur</span><span class="sxs-lookup"><span data-stu-id="af675-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="af675-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af675-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>] [-Zone <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af675-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="af675-105">DESCRIPTION</span></span>
<span data-ttu-id="af675-106">**New-AzPublicIpPrefix** cmdlet 'i genel bir IP öneki oluşturur.</span><span class="sxs-lookup"><span data-stu-id="af675-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="af675-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af675-107">EXAMPLES</span></span>

### <span data-ttu-id="af675-108">Örnek 1: yeni bir genel IP öneki oluşturma</span><span class="sxs-lookup"><span data-stu-id="af675-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="af675-109">Bu komut yeni bir genel IP öneki kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="af675-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="af675-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af675-110">PARAMETERS</span></span>

### <span data-ttu-id="af675-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="af675-111">-AsJob</span></span>
<span data-ttu-id="af675-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="af675-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af675-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af675-113">-DefaultProfile</span></span>
<span data-ttu-id="af675-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af675-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af675-115">-Force</span><span class="sxs-lookup"><span data-stu-id="af675-115">-Force</span></span>
<span data-ttu-id="af675-116">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="af675-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="af675-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="af675-117">-IpAddressVersion</span></span>
<span data-ttu-id="af675-118">Genel IP adresi sürümü.</span><span class="sxs-lookup"><span data-stu-id="af675-118">The public IP address version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af675-119">-Ipetiketi</span><span class="sxs-lookup"><span data-stu-id="af675-119">-IpTag</span></span>
<span data-ttu-id="af675-120">Iptag listesi.</span><span class="sxs-lookup"><span data-stu-id="af675-120">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af675-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="af675-121">-Location</span></span>
<span data-ttu-id="af675-122">Genel IP öneki konumu.</span><span class="sxs-lookup"><span data-stu-id="af675-122">The public IP prefix location.</span></span>

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

### <span data-ttu-id="af675-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="af675-123">-Name</span></span>
<span data-ttu-id="af675-124">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="af675-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af675-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="af675-125">-PrefixLength</span></span>
<span data-ttu-id="af675-126">Publicıpprefix uzunluğu</span><span class="sxs-lookup"><span data-stu-id="af675-126">The PublicIPPrefix length</span></span>

```yaml
Type: System.UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af675-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af675-127">-ResourceGroupName</span></span>
<span data-ttu-id="af675-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="af675-128">The resource group name.</span></span>

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

### <span data-ttu-id="af675-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="af675-129">-Sku</span></span>
<span data-ttu-id="af675-130">Genel IP öneki SKU adı.</span><span class="sxs-lookup"><span data-stu-id="af675-130">The public IP Prefix Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af675-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="af675-131">-Tag</span></span>
<span data-ttu-id="af675-132">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="af675-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="af675-133">-Bölge</span><span class="sxs-lookup"><span data-stu-id="af675-133">-Zone</span></span>
<span data-ttu-id="af675-134">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="af675-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="af675-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="af675-135">-Confirm</span></span>
<span data-ttu-id="af675-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="af675-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af675-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af675-137">-WhatIf</span></span>
<span data-ttu-id="af675-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="af675-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af675-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="af675-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af675-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af675-140">CommonParameters</span></span>
<span data-ttu-id="af675-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af675-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af675-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af675-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af675-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af675-143">INPUTS</span></span>

### <span data-ttu-id="af675-144">System. String</span><span class="sxs-lookup"><span data-stu-id="af675-144">System.String</span></span>

### <span data-ttu-id="af675-145">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="af675-145">System.UInt16</span></span>

### <span data-ttu-id="af675-146">Microsoft. Azure. Commands. Network. modeller. PSPublicIpPrefixTag []</span><span class="sxs-lookup"><span data-stu-id="af675-146">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="af675-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="af675-147">System.String[]</span></span>

### <span data-ttu-id="af675-148">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="af675-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="af675-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af675-149">OUTPUTS</span></span>

### <span data-ttu-id="af675-150">Microsoft. Azure. Commands. Network. model. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="af675-150">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="af675-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af675-151">NOTES</span></span>

## <span data-ttu-id="af675-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af675-152">RELATED LINKS</span></span>

[<span data-ttu-id="af675-153">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="af675-153">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="af675-154">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="af675-154">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="af675-155">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="af675-155">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
