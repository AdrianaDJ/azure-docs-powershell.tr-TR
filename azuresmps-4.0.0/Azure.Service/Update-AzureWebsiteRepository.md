---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: EFBC8DCD-00CC-4BBF-9383-EA15376535F3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42780f62bc68659874f7aae1e64ad5ce89038fdf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105843"
---
# <span data-ttu-id="a2dfb-101">Update-AzureWebsiteRepository</span><span class="sxs-lookup"><span data-stu-id="a2dfb-101">Update-AzureWebsiteRepository</span></span>

## <span data-ttu-id="a2dfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="a2dfb-103">Tüm yuvalar için yerel bir git deposunun uzaktaki depolarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a2dfb-103">Updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="a2dfb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2dfb-104">SYNTAX</span></span>

```
Update-AzureWebsiteRepository [-Name <String>] -PublishingUsername <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2dfb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2dfb-105">DESCRIPTION</span></span>
<span data-ttu-id="a2dfb-106">**Update-AzureWebsiteRepository** cmdlet 'i, tüm yuvalar için yerel bir git deposunun uzaktaki depolarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a2dfb-106">The **Update-AzureWebsiteRepository** cmdlet updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="a2dfb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2dfb-107">EXAMPLES</span></span>

### <span data-ttu-id="a2dfb-108">Örnek 1: Web sitesi uzak depolarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a2dfb-108">Example 1: Update Website Remote Repositories</span></span>
```
PS C:\> Update-AzureWebsiteRepository -Name MyWebsite
```

<span data-ttu-id="a2dfb-109">Tüm Web sitesi için tüm yuvalar Web sitesi</span><span class="sxs-lookup"><span data-stu-id="a2dfb-109">Updates the remote repositories of a local git repository for all the slots for website MyWebsite.</span></span>

## <span data-ttu-id="a2dfb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2dfb-110">PARAMETERS</span></span>

### <span data-ttu-id="a2dfb-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="a2dfb-111">-Name</span></span>
<span data-ttu-id="a2dfb-112">Web sitesinin adı.</span><span class="sxs-lookup"><span data-stu-id="a2dfb-112">The name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2dfb-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="a2dfb-113">-Profile</span></span>
<span data-ttu-id="a2dfb-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2dfb-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a2dfb-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a2dfb-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a2dfb-116">-Publishingkullanıcıadı</span><span class="sxs-lookup"><span data-stu-id="a2dfb-116">-PublishingUsername</span></span>
<span data-ttu-id="a2dfb-117">Git dağıtımı için Microsoft Azure portalında belirttiğiniz Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="a2dfb-117">The username you have specified in the Microsoft Azure Portal for Git deployment.</span></span>

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

### <span data-ttu-id="a2dfb-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="a2dfb-118">-Confirm</span></span>
<span data-ttu-id="a2dfb-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a2dfb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2dfb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2dfb-120">-WhatIf</span></span>
<span data-ttu-id="a2dfb-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2dfb-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2dfb-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a2dfb-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2dfb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2dfb-123">CommonParameters</span></span>
<span data-ttu-id="a2dfb-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2dfb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2dfb-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2dfb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2dfb-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2dfb-126">INPUTS</span></span>

## <span data-ttu-id="a2dfb-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2dfb-127">OUTPUTS</span></span>

## <span data-ttu-id="a2dfb-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2dfb-128">NOTES</span></span>

## <span data-ttu-id="a2dfb-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2dfb-129">RELATED LINKS</span></span>

[<span data-ttu-id="a2dfb-130">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a2dfb-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="a2dfb-131">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a2dfb-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="a2dfb-132">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a2dfb-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="a2dfb-133">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a2dfb-133">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


