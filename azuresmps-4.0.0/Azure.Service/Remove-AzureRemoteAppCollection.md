---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8E67D1A4-4247-4603-8D26-42D6D48FE686
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90c654432760061d5c2ba36675c958135329b225
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105868"
---
# <span data-ttu-id="4a7f2-101">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="4a7f2-101">Remove-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="4a7f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a7f2-102">SYNOPSIS</span></span>
<span data-ttu-id="4a7f2-103">Azure RemoteApp koleksiyonunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4a7f2-103">Removes an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="4a7f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a7f2-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppCollection [-CollectionName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a7f2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a7f2-105">DESCRIPTION</span></span>
<span data-ttu-id="4a7f2-106">**Remove-AzureRemoteAppCollection** cmdlet 'ı bir Azure RemoteApp koleksiyonunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4a7f2-106">The **Remove-AzureRemoteAppCollection** cmdlet removes an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="4a7f2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a7f2-107">EXAMPLES</span></span>

## <span data-ttu-id="4a7f2-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a7f2-108">PARAMETERS</span></span>

### <span data-ttu-id="4a7f2-109">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="4a7f2-109">-CollectionName</span></span>
<span data-ttu-id="4a7f2-110">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a7f2-110">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a7f2-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="4a7f2-111">-Profile</span></span>
<span data-ttu-id="4a7f2-112">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a7f2-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4a7f2-113">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="4a7f2-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4a7f2-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="4a7f2-114">-Confirm</span></span>
<span data-ttu-id="4a7f2-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4a7f2-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a7f2-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a7f2-116">-WhatIf</span></span>
<span data-ttu-id="4a7f2-117">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4a7f2-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a7f2-118">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4a7f2-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a7f2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a7f2-119">CommonParameters</span></span>
<span data-ttu-id="4a7f2-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a7f2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a7f2-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a7f2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a7f2-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a7f2-122">INPUTS</span></span>

## <span data-ttu-id="4a7f2-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a7f2-123">OUTPUTS</span></span>

## <span data-ttu-id="4a7f2-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a7f2-124">NOTES</span></span>

## <span data-ttu-id="4a7f2-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a7f2-125">RELATED LINKS</span></span>

[<span data-ttu-id="4a7f2-126">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="4a7f2-126">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="4a7f2-127">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="4a7f2-127">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="4a7f2-128">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="4a7f2-128">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="4a7f2-129">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="4a7f2-129">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


