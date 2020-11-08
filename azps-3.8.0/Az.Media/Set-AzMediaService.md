---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
ms.openlocfilehash: 5b85e3e64b4a79b33975d9b29d0498ac8ae0ce03
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104533"
---
# <span data-ttu-id="1a822-101">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1a822-101">Set-AzMediaService</span></span>

## <span data-ttu-id="1a822-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a822-102">SYNOPSIS</span></span>
<span data-ttu-id="1a822-103">Var olan medya hizmetlerinin belirtilen özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1a822-103">Modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="1a822-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a822-104">SYNTAX</span></span>

```
Set-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a822-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a822-105">DESCRIPTION</span></span>
<span data-ttu-id="1a822-106">**Set-AzMediaService** cmdlet 'i, var olan medya hizmetlerinin belirtilen özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1a822-106">The **Set-AzMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="1a822-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a822-107">EXAMPLES</span></span>

### <span data-ttu-id="1a822-108">Örnek 1: var olan medya hizmetini değiştirme</span><span class="sxs-lookup"><span data-stu-id="1a822-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tag $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="1a822-109">İlk komut bir dizi etiket oluşturur ve bu etiketleri $Tags adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="1a822-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="1a822-110">Bu ikinci komut, $Tags değişkeninde depolanan etiketlerle ResourceGroup123 adındaki kaynak grubuna ait olan MediaService001 adındaki medya hizmetini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1a822-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="1a822-111">Komut ayrıca $StorageAccounts değişkeninde depolanan bir dizi yapılandırma nesnesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="1a822-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="1a822-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a822-112">PARAMETERS</span></span>

### <span data-ttu-id="1a822-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1a822-113">-AccountName</span></span>
<span data-ttu-id="1a822-114">Bu cmdlet 'in değiştirdiği medya hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a822-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1a822-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a822-115">-DefaultProfile</span></span>
<span data-ttu-id="1a822-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1a822-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a822-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a822-117">-ResourceGroupName</span></span>
<span data-ttu-id="1a822-118">Medya hizmeti 'ni içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a822-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="1a822-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="1a822-119">-StorageAccounts</span></span>
<span data-ttu-id="1a822-120">Bu cmdlet 'in medya hizmetiyle ilişki kurduğu bir depolama hesapları dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a822-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a822-121">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1a822-121">-Tag</span></span>
<span data-ttu-id="1a822-122">Medya hesabıyla ilişkili Etiketler.</span><span class="sxs-lookup"><span data-stu-id="1a822-122">The tags associated with the media account.</span></span>

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

### <span data-ttu-id="1a822-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="1a822-123">-Confirm</span></span>
<span data-ttu-id="1a822-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1a822-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a822-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a822-125">-WhatIf</span></span>
<span data-ttu-id="1a822-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a822-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a822-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1a822-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a822-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a822-128">CommonParameters</span></span>
<span data-ttu-id="1a822-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a822-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a822-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a822-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a822-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a822-131">INPUTS</span></span>

### <span data-ttu-id="1a822-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1a822-132">System.String</span></span>

### <span data-ttu-id="1a822-133">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1a822-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1a822-134">Microsoft. Azure. Commands. Media. modeller. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="1a822-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="1a822-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a822-135">OUTPUTS</span></span>

### <span data-ttu-id="1a822-136">Microsoft. Azure. Commands. Media. modeller. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="1a822-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="1a822-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a822-137">NOTES</span></span>

## <span data-ttu-id="1a822-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a822-138">RELATED LINKS</span></span>

[<span data-ttu-id="1a822-139">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1a822-139">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="1a822-140">Yeni-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1a822-140">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="1a822-141">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1a822-141">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)


