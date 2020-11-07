---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
ms.openlocfilehash: d035890f6478c0b7fd767f12b8f9a27d4f765837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915752"
---
# <span data-ttu-id="acf8e-101">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="acf8e-101">Set-AzMediaService</span></span>

## <span data-ttu-id="acf8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acf8e-102">SYNOPSIS</span></span>
<span data-ttu-id="acf8e-103">Var olan medya hizmetlerinin belirtilen özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="acf8e-103">Modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="acf8e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="acf8e-104">SYNTAX</span></span>

```
Set-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="acf8e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="acf8e-105">DESCRIPTION</span></span>
<span data-ttu-id="acf8e-106">**Set-AzMediaService** cmdlet 'i, var olan medya hizmetlerinin belirtilen özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="acf8e-106">The **Set-AzMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="acf8e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="acf8e-107">EXAMPLES</span></span>

### <span data-ttu-id="acf8e-108">Örnek 1: var olan medya hizmetini değiştirme</span><span class="sxs-lookup"><span data-stu-id="acf8e-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tag $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="acf8e-109">İlk komut bir dizi etiket oluşturur ve bu etiketleri $Tags adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="acf8e-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="acf8e-110">Bu ikinci komut, $Tags değişkeninde depolanan etiketlerle ResourceGroup123 adındaki kaynak grubuna ait olan MediaService001 adındaki medya hizmetini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="acf8e-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="acf8e-111">Komut ayrıca $StorageAccounts değişkeninde depolanan bir dizi yapılandırma nesnesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="acf8e-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="acf8e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="acf8e-112">PARAMETERS</span></span>

### <span data-ttu-id="acf8e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="acf8e-113">-AccountName</span></span>
<span data-ttu-id="acf8e-114">Bu cmdlet 'in değiştirdiği medya hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acf8e-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="acf8e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf8e-115">-DefaultProfile</span></span>
<span data-ttu-id="acf8e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="acf8e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acf8e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf8e-117">-ResourceGroupName</span></span>
<span data-ttu-id="acf8e-118">Medya hizmeti 'ni içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acf8e-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="acf8e-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="acf8e-119">-StorageAccounts</span></span>
<span data-ttu-id="acf8e-120">Bu cmdlet 'in medya hizmetiyle ilişki kurduğu bir depolama hesapları dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="acf8e-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

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

### <span data-ttu-id="acf8e-121">Etiketli</span><span class="sxs-lookup"><span data-stu-id="acf8e-121">-Tag</span></span>
<span data-ttu-id="acf8e-122">Medya hesabıyla ilişkili Etiketler.</span><span class="sxs-lookup"><span data-stu-id="acf8e-122">The tags associated with the media account.</span></span>

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

### <span data-ttu-id="acf8e-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="acf8e-123">-Confirm</span></span>
<span data-ttu-id="acf8e-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="acf8e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acf8e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acf8e-125">-WhatIf</span></span>
<span data-ttu-id="acf8e-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="acf8e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acf8e-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="acf8e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acf8e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf8e-128">CommonParameters</span></span>
<span data-ttu-id="acf8e-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="acf8e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf8e-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acf8e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf8e-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="acf8e-131">INPUTS</span></span>

### <span data-ttu-id="acf8e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="acf8e-132">System.String</span></span>

### <span data-ttu-id="acf8e-133">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="acf8e-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="acf8e-134">Microsoft. Azure. Commands. Media. modeller. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="acf8e-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="acf8e-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="acf8e-135">OUTPUTS</span></span>

### <span data-ttu-id="acf8e-136">Microsoft. Azure. Commands. Media. modeller. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="acf8e-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="acf8e-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="acf8e-137">NOTES</span></span>

## <span data-ttu-id="acf8e-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="acf8e-138">RELATED LINKS</span></span>

[<span data-ttu-id="acf8e-139">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="acf8e-139">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="acf8e-140">Yeni-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="acf8e-140">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="acf8e-141">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="acf8e-141">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)


