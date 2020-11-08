---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B35979E5-94C4-4DCC-B87D-D6915464CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91d464abcd8b67a0fff2cd897fa6f45fe6cb3d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106149"
---
# <span data-ttu-id="2467d-101">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="2467d-101">Remove-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="2467d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2467d-102">SYNOPSIS</span></span>
<span data-ttu-id="2467d-103">Azure RemoteApp şablonu resmini siler.</span><span class="sxs-lookup"><span data-stu-id="2467d-103">Deletes an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="2467d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2467d-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppTemplateImage [-ImageName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2467d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2467d-105">DESCRIPTION</span></span>
<span data-ttu-id="2467d-106">**Remove-Azureremoteapptemplateımage** cmdlet 'ı bir Azure RemoteApp şablonu resmini siler.</span><span class="sxs-lookup"><span data-stu-id="2467d-106">The **Remove-AzureRemoteAppTemplateImage** cmdlet deletes an Azure RemoteApp template image.</span></span>
<span data-ttu-id="2467d-107">Bir şablon görüntüsü yalnızca herhangi bir Azure RemoteApp koleksiyonuna bağlı değilse silinebilir.</span><span class="sxs-lookup"><span data-stu-id="2467d-107">A template image can deleted only if it is not linked to any Azure RemoteApp collection.</span></span>

## <span data-ttu-id="2467d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2467d-108">EXAMPLES</span></span>

### <span data-ttu-id="2467d-109">Örnek 1: şablon görüntüsü silme</span><span class="sxs-lookup"><span data-stu-id="2467d-109">Example 1: Delete a template image</span></span>
```
PS C:\> Remove-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="2467d-110">Bu komut, ContosoApps adlı şablon resmini siler.</span><span class="sxs-lookup"><span data-stu-id="2467d-110">This command deletes the template image named ContosoApps.</span></span>

## <span data-ttu-id="2467d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2467d-111">PARAMETERS</span></span>

### <span data-ttu-id="2467d-112">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="2467d-112">-ImageName</span></span>
<span data-ttu-id="2467d-113">RemoteApp şablonu görüntüsünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2467d-113">Specifies the name of the RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2467d-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="2467d-114">-Profile</span></span>
<span data-ttu-id="2467d-115">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2467d-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2467d-116">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="2467d-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2467d-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="2467d-117">-Confirm</span></span>
<span data-ttu-id="2467d-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2467d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2467d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2467d-119">-WhatIf</span></span>
<span data-ttu-id="2467d-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2467d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2467d-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2467d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2467d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2467d-122">CommonParameters</span></span>
<span data-ttu-id="2467d-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2467d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2467d-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2467d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2467d-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2467d-125">INPUTS</span></span>

## <span data-ttu-id="2467d-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2467d-126">OUTPUTS</span></span>

## <span data-ttu-id="2467d-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2467d-127">NOTES</span></span>

## <span data-ttu-id="2467d-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2467d-128">RELATED LINKS</span></span>

[<span data-ttu-id="2467d-129">Get-Azureremoteapptemplateımage</span><span class="sxs-lookup"><span data-stu-id="2467d-129">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="2467d-130">Yeni-Azureremoteapptemplateımage</span><span class="sxs-lookup"><span data-stu-id="2467d-130">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="2467d-131">Rename-Azureremoteapptemplateımage</span><span class="sxs-lookup"><span data-stu-id="2467d-131">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


