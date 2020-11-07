---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
ms.openlocfilehash: d52bc8737392bf6fce004a90b1f2fe5207cffea9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764613"
---
# <span data-ttu-id="cef3c-101">New-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cef3c-101">New-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="cef3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cef3c-102">SYNOPSIS</span></span>
<span data-ttu-id="cef3c-103">Genel bir IP öneki oluşturur</span><span class="sxs-lookup"><span data-stu-id="cef3c-103">Creates a Public IP Prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cef3c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cef3c-104">SYNTAX</span></span>

```
New-AzureRmPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cef3c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cef3c-105">DESCRIPTION</span></span>
<span data-ttu-id="cef3c-106">**Yeni-AzureRmPublicIpPrefix** cmdlet 'i genel bir IP öneki oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cef3c-106">The **New-AzureRmPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="cef3c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cef3c-107">EXAMPLES</span></span>

### <span data-ttu-id="cef3c-108">1: yeni bir genel IP öneki oluşturma</span><span class="sxs-lookup"><span data-stu-id="cef3c-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="cef3c-109">Bu komut yeni bir genel IP öneki kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cef3c-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="cef3c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cef3c-110">PARAMETERS</span></span>

### <span data-ttu-id="cef3c-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="cef3c-111">-AsJob</span></span>
<span data-ttu-id="cef3c-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="cef3c-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef3c-113">-DefaultProfile</span></span>
<span data-ttu-id="cef3c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cef3c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef3c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cef3c-115">-Force</span></span>
<span data-ttu-id="cef3c-116">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="cef3c-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef3c-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="cef3c-117">-IpAddressVersion</span></span>
<span data-ttu-id="cef3c-118">Genel IP adresi sürümü.</span><span class="sxs-lookup"><span data-stu-id="cef3c-118">The public IP address version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef3c-119">-Ipetiketi</span><span class="sxs-lookup"><span data-stu-id="cef3c-119">-IpTag</span></span>
<span data-ttu-id="cef3c-120">Iptag listesi.</span><span class="sxs-lookup"><span data-stu-id="cef3c-120">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef3c-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="cef3c-121">-Location</span></span>
<span data-ttu-id="cef3c-122">Genel IP öneki konumu.</span><span class="sxs-lookup"><span data-stu-id="cef3c-122">The public IP prefix location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef3c-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="cef3c-123">-Name</span></span>
<span data-ttu-id="cef3c-124">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="cef3c-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef3c-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="cef3c-125">-PrefixLength</span></span>
<span data-ttu-id="cef3c-126">Publicıpprefix uzunluğu</span><span class="sxs-lookup"><span data-stu-id="cef3c-126">The PublicIPPrefix length</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef3c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cef3c-127">-ResourceGroupName</span></span>
<span data-ttu-id="cef3c-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cef3c-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef3c-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="cef3c-129">-Sku</span></span>
<span data-ttu-id="cef3c-130">Genel IP öneki SKU adı.</span><span class="sxs-lookup"><span data-stu-id="cef3c-130">The public IP Prefix Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef3c-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="cef3c-131">-Tag</span></span>
<span data-ttu-id="cef3c-132">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="cef3c-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef3c-133">-Bölge</span><span class="sxs-lookup"><span data-stu-id="cef3c-133">-Zone</span></span>
<span data-ttu-id="cef3c-134">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="cef3c-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef3c-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="cef3c-135">-Confirm</span></span>
<span data-ttu-id="cef3c-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cef3c-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef3c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cef3c-137">-WhatIf</span></span>
<span data-ttu-id="cef3c-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cef3c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cef3c-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cef3c-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef3c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef3c-140">CommonParameters</span></span>
<span data-ttu-id="cef3c-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cef3c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cef3c-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cef3c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef3c-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cef3c-143">INPUTS</span></span>

### <span data-ttu-id="cef3c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="cef3c-144">System.String</span></span>
<span data-ttu-id="cef3c-145">System. UInt16 System. Koleksiyonlar. Generic. List `1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List` 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cef3c-145">System.UInt16 System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="cef3c-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cef3c-146">OUTPUTS</span></span>

### <span data-ttu-id="cef3c-147">Microsoft. Azure. Commands. Network. model. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cef3c-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="cef3c-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cef3c-148">NOTES</span></span>

## <span data-ttu-id="cef3c-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cef3c-149">RELATED LINKS</span></span>
