---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 5af78bb1f915dec55f75749296340ca6d13a3b3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274115"
---
# <span data-ttu-id="cfb22-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cfb22-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="cfb22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfb22-102">SYNOPSIS</span></span>
<span data-ttu-id="cfb22-103">Bir Azure SecurityPartnerProvider oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cfb22-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="cfb22-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cfb22-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfb22-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cfb22-105">DESCRIPTION</span></span>
<span data-ttu-id="cfb22-106">**Yeni-AzSecurityPartnerProvider** cmdlet 'ı bir Azure securitypartnerprovider oluşturur</span><span class="sxs-lookup"><span data-stu-id="cfb22-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="cfb22-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cfb22-107">EXAMPLES</span></span>

### <span data-ttu-id="cfb22-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cfb22-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="cfb22-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cfb22-109">PARAMETERS</span></span>

### <span data-ttu-id="cfb22-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="cfb22-110">-AsJob</span></span>
<span data-ttu-id="cfb22-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="cfb22-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cfb22-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfb22-112">-DefaultProfile</span></span>
<span data-ttu-id="cfb22-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cfb22-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfb22-114">-Force</span><span class="sxs-lookup"><span data-stu-id="cfb22-114">-Force</span></span>
<span data-ttu-id="cfb22-115">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="cfb22-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="cfb22-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="cfb22-116">-Location</span></span>
<span data-ttu-id="cfb22-117">konumuyla.</span><span class="sxs-lookup"><span data-stu-id="cfb22-117">location.</span></span>

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

### <span data-ttu-id="cfb22-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="cfb22-118">-Name</span></span>
<span data-ttu-id="cfb22-119">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="cfb22-119">The resource name.</span></span>

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

### <span data-ttu-id="cfb22-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfb22-120">-ResourceGroupName</span></span>
<span data-ttu-id="cfb22-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cfb22-121">The resource group name.</span></span>

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

### <span data-ttu-id="cfb22-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="cfb22-122">-SecurityProviderName</span></span>
<span data-ttu-id="cfb22-123">Güvenlik sağlayıcı adı</span><span class="sxs-lookup"><span data-stu-id="cfb22-123">The Security Provider name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ZScaler, IBoss, Checkpoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfb22-124">Etiketli</span><span class="sxs-lookup"><span data-stu-id="cfb22-124">-Tag</span></span>
<span data-ttu-id="cfb22-125">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="cfb22-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="cfb22-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="cfb22-126">-VirtualHub</span></span>
<span data-ttu-id="cfb22-127">Güvenlik ortağı sağlayıcısının bağlı olduğu sanal hub kimliği</span><span class="sxs-lookup"><span data-stu-id="cfb22-127">The virtual hub Id that the security partner provider is attached to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfb22-128">-Virtualhubıd</span><span class="sxs-lookup"><span data-stu-id="cfb22-128">-VirtualHubId</span></span>
<span data-ttu-id="cfb22-129">Bu VpnGateway 'in ilişkilendirildiği VirtualHub kimliği.</span><span class="sxs-lookup"><span data-stu-id="cfb22-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="cfb22-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="cfb22-130">-VirtualHubName</span></span>
<span data-ttu-id="cfb22-131">Bu VpnGateway 'in ilişkilendirildiği VirtualHub kimliği.</span><span class="sxs-lookup"><span data-stu-id="cfb22-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="cfb22-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="cfb22-132">-Confirm</span></span>
<span data-ttu-id="cfb22-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cfb22-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfb22-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfb22-134">-WhatIf</span></span>
<span data-ttu-id="cfb22-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cfb22-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfb22-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cfb22-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfb22-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfb22-137">CommonParameters</span></span>
<span data-ttu-id="cfb22-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cfb22-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfb22-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cfb22-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfb22-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cfb22-140">INPUTS</span></span>

### <span data-ttu-id="cfb22-141">System. String</span><span class="sxs-lookup"><span data-stu-id="cfb22-141">System.String</span></span>

### <span data-ttu-id="cfb22-142">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cfb22-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="cfb22-143">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cfb22-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cfb22-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cfb22-144">OUTPUTS</span></span>

### <span data-ttu-id="cfb22-145">Microsoft. Azure. Commands. Network. model. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cfb22-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="cfb22-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cfb22-146">NOTES</span></span>

## <span data-ttu-id="cfb22-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cfb22-147">RELATED LINKS</span></span>
