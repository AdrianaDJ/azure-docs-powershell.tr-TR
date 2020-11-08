---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6E369BDF-AE3C-416B-81B7-097C20147CBE
online version: ''
schema: 2.0.0
ms.openlocfilehash: bb48f7412c957ceefb7df03d79e57ce8e75447d5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106130"
---
# <span data-ttu-id="ce47e-101">Remove-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="ce47e-101">Remove-AzureSBNamespace</span></span>

## <span data-ttu-id="ce47e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce47e-102">SYNOPSIS</span></span>
<span data-ttu-id="ce47e-103">Ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ce47e-103">Removes a namespace.</span></span>

## <span data-ttu-id="ce47e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce47e-104">SYNTAX</span></span>

```
Remove-AzureSBNamespace -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce47e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce47e-105">DESCRIPTION</span></span>
<span data-ttu-id="ce47e-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ce47e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ce47e-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ce47e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ce47e-108">**Remove-AzureSBNamespace** cmdlet 'ı, hizmet veri yolu için bir hizmet ad boşluğunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ce47e-108">The **Remove-AzureSBNamespace** cmdlet removes a service namespace for Service Bus.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="ce47e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce47e-109">EXAMPLES</span></span>

## <span data-ttu-id="ce47e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce47e-110">PARAMETERS</span></span>

### <span data-ttu-id="ce47e-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ce47e-111">-Force</span></span>
<span data-ttu-id="ce47e-112">Etkinse, onay istemeden ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ce47e-112">If enabled, removes the namespace without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ce47e-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="ce47e-113">-Name</span></span>
<span data-ttu-id="ce47e-114">Kaldırılacak ad alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce47e-114">Specifies the name of the namespace to be removed.</span></span>

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

### <span data-ttu-id="ce47e-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ce47e-115">-PassThru</span></span>
<span data-ttu-id="ce47e-116">İşlem başarılı olursa işlemin doğru döndürmesine neden olur.</span><span class="sxs-lookup"><span data-stu-id="ce47e-116">Causes the operation to return true if it succeeds.</span></span>

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

### <span data-ttu-id="ce47e-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="ce47e-117">-Profile</span></span>
<span data-ttu-id="ce47e-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce47e-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ce47e-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ce47e-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ce47e-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="ce47e-120">-Confirm</span></span>
<span data-ttu-id="ce47e-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ce47e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce47e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce47e-122">-WhatIf</span></span>
<span data-ttu-id="ce47e-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce47e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce47e-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ce47e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce47e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce47e-125">CommonParameters</span></span>
<span data-ttu-id="ce47e-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce47e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce47e-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce47e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce47e-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce47e-128">INPUTS</span></span>

## <span data-ttu-id="ce47e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce47e-129">OUTPUTS</span></span>

## <span data-ttu-id="ce47e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce47e-130">NOTES</span></span>

## <span data-ttu-id="ce47e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce47e-131">RELATED LINKS</span></span>

[<span data-ttu-id="ce47e-132">New-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="ce47e-132">New-AzureSBNamespace</span></span>](./New-AzureSBNamespace.md)


