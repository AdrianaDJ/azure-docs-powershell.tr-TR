---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D35C580F-437A-40F9-B6BA-412A1176292A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9821602df196604100de5926a7d9510bdb011bd2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105681"
---
# <span data-ttu-id="b74c6-101">Export-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b74c6-101">Export-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="b74c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b74c6-102">SYNOPSIS</span></span>
<span data-ttu-id="b74c6-103">Bir Azure RemoteApp koleksiyonunun şablon görüntüsünü belirtilen Azure depolama hesabına aktarır.</span><span class="sxs-lookup"><span data-stu-id="b74c6-103">Exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="b74c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b74c6-104">SYNTAX</span></span>

```
Export-AzureRemoteAppTemplateImage [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingTemplateImage] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b74c6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b74c6-105">DESCRIPTION</span></span>
<span data-ttu-id="b74c6-106">**Export-Azureremoteapptemplateımage** cmdlet 'i, bir Azure RemoteApp koleksiyonunun şablon görüntüsünü belirtilen Azure depolama hesabına aktarır.</span><span class="sxs-lookup"><span data-stu-id="b74c6-106">The **Export-AzureRemoteAppTemplateImage** cmdlet exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="b74c6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b74c6-107">EXAMPLES</span></span>

### <span data-ttu-id="b74c6-108">Örnek 1: Azure depolama hesabına bir şablon görüntüsü dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="b74c6-108">Example 1: Export a template image to the Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppTemplateImage -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingTemplateImage
```

<span data-ttu-id="b74c6-109">Bu komut contoso adlı koleksiyonun şablon resmini belirtilen Azure depolama hesabında Name AccountName ve Key AccountKey ile birlikte dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="b74c6-109">This command exports the template image of the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="b74c6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b74c6-110">PARAMETERS</span></span>

### <span data-ttu-id="b74c6-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="b74c6-111">-CollectionName</span></span>
<span data-ttu-id="b74c6-112">Kaynak Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b74c6-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b74c6-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="b74c6-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="b74c6-114">Hedef Azure depolama hesabında bir kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b74c6-114">Specifies the name of a container in the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b74c6-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b74c6-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="b74c6-116">Hedef Azure depolama hesabının anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b74c6-116">Specifies the key of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b74c6-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b74c6-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="b74c6-118">Hedef Azure depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b74c6-118">Specifies the name of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b74c6-119">-Overwriteexistingtemplateımage</span><span class="sxs-lookup"><span data-stu-id="b74c6-119">-OverwriteExistingTemplateImage</span></span>
<span data-ttu-id="b74c6-120">Cmdlet 'in var olan şablon resminin üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b74c6-120">Indicates that the cmdlet overwrites the existing template image.</span></span>

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

### <span data-ttu-id="b74c6-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="b74c6-121">-Profile</span></span>
<span data-ttu-id="b74c6-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b74c6-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b74c6-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b74c6-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74c6-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="b74c6-124">-Confirm</span></span>
<span data-ttu-id="b74c6-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b74c6-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74c6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b74c6-126">-WhatIf</span></span>
<span data-ttu-id="b74c6-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b74c6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b74c6-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b74c6-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74c6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b74c6-129">CommonParameters</span></span>
<span data-ttu-id="b74c6-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b74c6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b74c6-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b74c6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b74c6-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b74c6-132">INPUTS</span></span>

## <span data-ttu-id="b74c6-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b74c6-133">OUTPUTS</span></span>

## <span data-ttu-id="b74c6-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b74c6-134">NOTES</span></span>

## <span data-ttu-id="b74c6-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b74c6-135">RELATED LINKS</span></span>

[<span data-ttu-id="b74c6-136">Get-Azureremoteapptemplateımage</span><span class="sxs-lookup"><span data-stu-id="b74c6-136">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="b74c6-137">Yeni-Azureremoteapptemplateımage</span><span class="sxs-lookup"><span data-stu-id="b74c6-137">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="b74c6-138">Remove-Azureremoteapptemplateımage</span><span class="sxs-lookup"><span data-stu-id="b74c6-138">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="b74c6-139">Rename-Azureremoteapptemplateımage</span><span class="sxs-lookup"><span data-stu-id="b74c6-139">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


