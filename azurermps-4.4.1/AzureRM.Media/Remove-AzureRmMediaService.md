---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
ms.openlocfilehash: 9507cc178613a80ff0d49ed62e7e43698f5f1d7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763699"
---
# <span data-ttu-id="67c7b-101">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="67c7b-101">Remove-AzureRmMediaService</span></span>

## <span data-ttu-id="67c7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67c7b-102">SYNOPSIS</span></span>
<span data-ttu-id="67c7b-103">Medya hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67c7b-103">Removes a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67c7b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67c7b-104">SYNTAX</span></span>

```
Remove-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67c7b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="67c7b-105">DESCRIPTION</span></span>
<span data-ttu-id="67c7b-106">**Remove-AzureRmMediaService** cmdlet 'i bir medya hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67c7b-106">The **Remove-AzureRmMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="67c7b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67c7b-107">EXAMPLES</span></span>

### <span data-ttu-id="67c7b-108">Örnek 1: medya hizmetini kaldırma</span><span class="sxs-lookup"><span data-stu-id="67c7b-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzureRmMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="67c7b-109">Bu komut, ResourceGroup001 adındaki kaynak grubundaki MediaService0011 adındaki medya hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67c7b-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="67c7b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67c7b-110">PARAMETERS</span></span>

### <span data-ttu-id="67c7b-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="67c7b-111">-AccountName</span></span>
<span data-ttu-id="67c7b-112">Bu cmdlet 'in kaldırdığı medya hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67c7b-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="67c7b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="67c7b-113">-Force</span></span>
<span data-ttu-id="67c7b-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="67c7b-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="67c7b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67c7b-115">-ResourceGroupName</span></span>
<span data-ttu-id="67c7b-116">Medya hizmeti 'ni içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67c7b-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="67c7b-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="67c7b-117">-Confirm</span></span>
<span data-ttu-id="67c7b-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="67c7b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67c7b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67c7b-119">-WhatIf</span></span>
<span data-ttu-id="67c7b-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="67c7b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67c7b-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="67c7b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67c7b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67c7b-122">-DefaultProfile</span></span>
<span data-ttu-id="67c7b-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="67c7b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67c7b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67c7b-124">CommonParameters</span></span>
<span data-ttu-id="67c7b-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67c7b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67c7b-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67c7b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67c7b-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67c7b-127">INPUTS</span></span>

## <span data-ttu-id="67c7b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67c7b-128">OUTPUTS</span></span>

### <span data-ttu-id="67c7b-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="67c7b-129">System.Boolean</span></span>

## <span data-ttu-id="67c7b-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67c7b-130">NOTES</span></span>

## <span data-ttu-id="67c7b-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67c7b-131">RELATED LINKS</span></span>

[<span data-ttu-id="67c7b-132">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="67c7b-132">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="67c7b-133">Yeni-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="67c7b-133">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="67c7b-134">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="67c7b-134">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


