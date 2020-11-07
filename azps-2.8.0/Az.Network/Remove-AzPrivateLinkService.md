---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: 3b0ba9527ca7d0354429a90439bbe33d973bf550
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918040"
---
# <span data-ttu-id="52115-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="52115-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="52115-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52115-102">SYNOPSIS</span></span>
<span data-ttu-id="52115-103">Özel bağlantı hizmetini kaldırır</span><span class="sxs-lookup"><span data-stu-id="52115-103">Removes a private link service</span></span>

## <span data-ttu-id="52115-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52115-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52115-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="52115-105">DESCRIPTION</span></span>
<span data-ttu-id="52115-106">**Remove-AzPrivateLinkService** cmdlet 'i özel bir bağlantı hizmetini kaldırıyor</span><span class="sxs-lookup"><span data-stu-id="52115-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="52115-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52115-107">EXAMPLES</span></span>

### <span data-ttu-id="52115-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="52115-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="52115-109">Bu örnek TestPrivateLinkService adındaki özel bağlantı hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="52115-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="52115-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52115-110">PARAMETERS</span></span>

### <span data-ttu-id="52115-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="52115-111">-AsJob</span></span>
<span data-ttu-id="52115-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="52115-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52115-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52115-113">-DefaultProfile</span></span>
<span data-ttu-id="52115-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52115-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52115-115">-Force</span><span class="sxs-lookup"><span data-stu-id="52115-115">-Force</span></span>
<span data-ttu-id="52115-116">Kaynağı silmek istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="52115-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="52115-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="52115-117">-Name</span></span>
<span data-ttu-id="52115-118">Hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="52115-118">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52115-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="52115-119">-PassThru</span></span>
<span data-ttu-id="52115-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="52115-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="52115-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="52115-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="52115-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52115-122">-ResourceGroupName</span></span>
<span data-ttu-id="52115-123">Özel bağlantı hizmetinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="52115-123">The resource group name of the private link service.</span></span>

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

### <span data-ttu-id="52115-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="52115-124">-Confirm</span></span>
<span data-ttu-id="52115-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="52115-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52115-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52115-126">-WhatIf</span></span>
<span data-ttu-id="52115-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="52115-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52115-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="52115-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52115-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52115-129">CommonParameters</span></span>
<span data-ttu-id="52115-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52115-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52115-131">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="52115-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52115-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52115-132">INPUTS</span></span>

### <span data-ttu-id="52115-133">System. String</span><span class="sxs-lookup"><span data-stu-id="52115-133">System.String</span></span>

## <span data-ttu-id="52115-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52115-134">OUTPUTS</span></span>

### <span data-ttu-id="52115-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52115-135">System.Boolean</span></span>

## <span data-ttu-id="52115-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52115-136">NOTES</span></span>

## <span data-ttu-id="52115-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52115-137">RELATED LINKS</span></span>

[<span data-ttu-id="52115-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="52115-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="52115-139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="52115-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)