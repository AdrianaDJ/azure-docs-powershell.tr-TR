---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DB3F85D6-5962-4288-AD75-0C30448B769C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88438fa66e39b5ad63db7b6d2609107d224f7faf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106020"
---
# <span data-ttu-id="299e3-101">Unpublish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="299e3-101">Unpublish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="299e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="299e3-102">SYNOPSIS</span></span>
<span data-ttu-id="299e3-103">Bir Azure RemoteApp programını yayımdan kaldırma.</span><span class="sxs-lookup"><span data-stu-id="299e3-103">Unpublishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="299e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="299e3-104">SYNTAX</span></span>

```
Unpublish-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String[]>] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="299e3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="299e3-105">DESCRIPTION</span></span>
<span data-ttu-id="299e3-106">**Yayımdan kaldırma-AzureRemoteAppProgram** cmdlet 'ı bir Azure RemoteApp programını yayımlıyor.</span><span class="sxs-lookup"><span data-stu-id="299e3-106">The **Unpublish-AzureRemoteAppProgram** cmdlet unpublishes an Azure RemoteApp program.</span></span>
<span data-ttu-id="299e3-107">Bir programı yayımdan kaldırdıktan sonra, artık Azure RemoteApp koleksiyonu kullanıcıları tarafından kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="299e3-107">After you unpublish a program, it is no longer available to the users of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="299e3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="299e3-108">EXAMPLES</span></span>

## <span data-ttu-id="299e3-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="299e3-109">PARAMETERS</span></span>

### <span data-ttu-id="299e3-110">-Diğer ad</span><span class="sxs-lookup"><span data-stu-id="299e3-110">-Alias</span></span>
<span data-ttu-id="299e3-111">Programların yayımdan kaldırılması için bir diğer ad dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="299e3-111">Specifies an array of aliases of the programs to unpublish.</span></span>
<span data-ttu-id="299e3-112">Bir programın diğer adını yayımdan kaldırmak için **Get-AzureRemoteAppProgram** 'ı kullanın.</span><span class="sxs-lookup"><span data-stu-id="299e3-112">Use **Get-AzureRemoteAppProgram** to retrieve the alias of a program to unpublish.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="299e3-113">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="299e3-113">-CollectionName</span></span>
<span data-ttu-id="299e3-114">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="299e3-114">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="299e3-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="299e3-115">-Profile</span></span>
<span data-ttu-id="299e3-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="299e3-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="299e3-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="299e3-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="299e3-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="299e3-118">-Confirm</span></span>
<span data-ttu-id="299e3-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="299e3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="299e3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="299e3-120">-WhatIf</span></span>
<span data-ttu-id="299e3-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="299e3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="299e3-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="299e3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="299e3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="299e3-123">CommonParameters</span></span>
<span data-ttu-id="299e3-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="299e3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="299e3-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="299e3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="299e3-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="299e3-126">INPUTS</span></span>

## <span data-ttu-id="299e3-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="299e3-127">OUTPUTS</span></span>

## <span data-ttu-id="299e3-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="299e3-128">NOTES</span></span>

## <span data-ttu-id="299e3-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="299e3-129">RELATED LINKS</span></span>

[<span data-ttu-id="299e3-130">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="299e3-130">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="299e3-131">Publish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="299e3-131">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)


