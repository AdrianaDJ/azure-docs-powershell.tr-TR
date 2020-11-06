---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/remove-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
ms.openlocfilehash: 9ddf8291d5f6276126cea82305bbc554d05ca006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593992"
---
# <span data-ttu-id="935b6-101">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="935b6-101">Remove-AzureRmMediaService</span></span>

## <span data-ttu-id="935b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="935b6-102">SYNOPSIS</span></span>
<span data-ttu-id="935b6-103">Medya hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="935b6-103">Removes a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="935b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="935b6-104">SYNTAX</span></span>

```
Remove-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="935b6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="935b6-105">DESCRIPTION</span></span>
<span data-ttu-id="935b6-106">**Remove-AzureRmMediaService** cmdlet 'i bir medya hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="935b6-106">The **Remove-AzureRmMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="935b6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="935b6-107">EXAMPLES</span></span>

### <span data-ttu-id="935b6-108">Örnek 1: medya hizmetini kaldırma</span><span class="sxs-lookup"><span data-stu-id="935b6-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzureRmMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="935b6-109">Bu komut, ResourceGroup001 adındaki kaynak grubundaki MediaService0011 adındaki medya hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="935b6-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="935b6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="935b6-110">PARAMETERS</span></span>

### <span data-ttu-id="935b6-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="935b6-111">-AccountName</span></span>
<span data-ttu-id="935b6-112">Bu cmdlet 'in kaldırdığı medya hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="935b6-112">Specifies the name of the media service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="935b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="935b6-113">-DefaultProfile</span></span>
<span data-ttu-id="935b6-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="935b6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="935b6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="935b6-115">-Force</span></span>
<span data-ttu-id="935b6-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="935b6-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="935b6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="935b6-117">-ResourceGroupName</span></span>
<span data-ttu-id="935b6-118">Medya hizmeti 'ni içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="935b6-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="935b6-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="935b6-119">-Confirm</span></span>
<span data-ttu-id="935b6-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="935b6-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="935b6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="935b6-121">-WhatIf</span></span>
<span data-ttu-id="935b6-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="935b6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="935b6-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="935b6-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="935b6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935b6-124">CommonParameters</span></span>
<span data-ttu-id="935b6-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="935b6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935b6-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="935b6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935b6-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="935b6-127">INPUTS</span></span>

### <span data-ttu-id="935b6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="935b6-128">System.String</span></span>

## <span data-ttu-id="935b6-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="935b6-129">OUTPUTS</span></span>

### <span data-ttu-id="935b6-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="935b6-130">System.Boolean</span></span>

## <span data-ttu-id="935b6-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="935b6-131">NOTES</span></span>

## <span data-ttu-id="935b6-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="935b6-132">RELATED LINKS</span></span>

[<span data-ttu-id="935b6-133">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="935b6-133">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="935b6-134">Yeni-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="935b6-134">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="935b6-135">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="935b6-135">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


