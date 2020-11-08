---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 1012bd4da163b992aec049643feb1e3fd8b4bf76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265920"
---
# <span data-ttu-id="2d814-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="2d814-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="2d814-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d814-102">SYNOPSIS</span></span>
<span data-ttu-id="2d814-103">DNS bölgesi grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2d814-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="2d814-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d814-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d814-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d814-105">DESCRIPTION</span></span>
<span data-ttu-id="2d814-106">**Remove-AzPrivateDnsZoneGroup** cmdlet 'ı bir DNS bölgesi grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2d814-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="2d814-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d814-107">EXAMPLES</span></span>

### <span data-ttu-id="2d814-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2d814-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="2d814-109">Yukarıdaki örnek, dnsgroup1 adlı bir DNS bölgesi</span><span class="sxs-lookup"><span data-stu-id="2d814-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="2d814-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d814-110">PARAMETERS</span></span>

### <span data-ttu-id="2d814-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="2d814-111">-AsJob</span></span>
<span data-ttu-id="2d814-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2d814-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d814-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d814-113">-DefaultProfile</span></span>
<span data-ttu-id="2d814-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2d814-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d814-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2d814-115">-Force</span></span>
<span data-ttu-id="2d814-116">Kaynağı silmek istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="2d814-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="2d814-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="2d814-117">-Name</span></span>
<span data-ttu-id="2d814-118">Özel DNS bölgesi grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2d814-118">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d814-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2d814-119">-PassThru</span></span>
<span data-ttu-id="2d814-120">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="2d814-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="2d814-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="2d814-121">-PrivateEndpointName</span></span>
<span data-ttu-id="2d814-122">Özel uç noktasının adı.</span><span class="sxs-lookup"><span data-stu-id="2d814-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="2d814-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d814-123">-ResourceGroupName</span></span>
<span data-ttu-id="2d814-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2d814-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="2d814-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="2d814-125">-Confirm</span></span>
<span data-ttu-id="2d814-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2d814-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d814-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d814-127">-WhatIf</span></span>
<span data-ttu-id="2d814-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2d814-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d814-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2d814-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d814-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d814-130">CommonParameters</span></span>
<span data-ttu-id="2d814-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d814-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d814-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2d814-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d814-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d814-133">INPUTS</span></span>

### <span data-ttu-id="2d814-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2d814-134">System.String</span></span>

## <span data-ttu-id="2d814-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d814-135">OUTPUTS</span></span>

### <span data-ttu-id="2d814-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d814-136">System.Boolean</span></span>

## <span data-ttu-id="2d814-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d814-137">NOTES</span></span>

## <span data-ttu-id="2d814-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d814-138">RELATED LINKS</span></span>
