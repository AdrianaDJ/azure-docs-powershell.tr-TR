---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: 525c5e2bfd15811e861945a6404e0b88274e2563
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109540"
---
# <span data-ttu-id="6fbad-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="6fbad-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="6fbad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fbad-102">SYNOPSIS</span></span>
<span data-ttu-id="6fbad-103">Medya hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6fbad-103">Removes a media service.</span></span>

## <span data-ttu-id="6fbad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6fbad-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fbad-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6fbad-105">DESCRIPTION</span></span>
<span data-ttu-id="6fbad-106">**Remove-AzMediaService** cmdlet 'i bir medya hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6fbad-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="6fbad-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6fbad-107">EXAMPLES</span></span>

### <span data-ttu-id="6fbad-108">Örnek 1: medya hizmetini kaldırma</span><span class="sxs-lookup"><span data-stu-id="6fbad-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="6fbad-109">Bu komut, ResourceGroup001 adındaki kaynak grubundaki MediaService0011 adındaki medya hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6fbad-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="6fbad-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6fbad-110">PARAMETERS</span></span>

### <span data-ttu-id="6fbad-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6fbad-111">-AccountName</span></span>
<span data-ttu-id="6fbad-112">Bu cmdlet 'in kaldırdığı medya hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6fbad-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6fbad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fbad-113">-DefaultProfile</span></span>
<span data-ttu-id="6fbad-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6fbad-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6fbad-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6fbad-115">-Force</span></span>
<span data-ttu-id="6fbad-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="6fbad-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6fbad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fbad-117">-ResourceGroupName</span></span>
<span data-ttu-id="6fbad-118">Medya hizmeti 'ni içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6fbad-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="6fbad-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="6fbad-119">-Confirm</span></span>
<span data-ttu-id="6fbad-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6fbad-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fbad-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fbad-121">-WhatIf</span></span>
<span data-ttu-id="6fbad-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6fbad-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fbad-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6fbad-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fbad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fbad-124">CommonParameters</span></span>
<span data-ttu-id="6fbad-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6fbad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fbad-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fbad-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fbad-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6fbad-127">INPUTS</span></span>

### <span data-ttu-id="6fbad-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6fbad-128">System.String</span></span>

## <span data-ttu-id="6fbad-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6fbad-129">OUTPUTS</span></span>

### <span data-ttu-id="6fbad-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6fbad-130">System.Boolean</span></span>

## <span data-ttu-id="6fbad-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6fbad-131">NOTES</span></span>

## <span data-ttu-id="6fbad-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6fbad-132">RELATED LINKS</span></span>

[<span data-ttu-id="6fbad-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="6fbad-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="6fbad-134">Yeni-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="6fbad-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="6fbad-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="6fbad-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


