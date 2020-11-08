---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 6496f2c65c5cfecb01ed68d0e47281fba72b7b63
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104459"
---
# <span data-ttu-id="76a82-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="76a82-101">New-AzADGroup</span></span>

## <span data-ttu-id="76a82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76a82-102">SYNOPSIS</span></span>
<span data-ttu-id="76a82-103">Yeni bir Active Directory grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76a82-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="76a82-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76a82-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76a82-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="76a82-105">DESCRIPTION</span></span>
<span data-ttu-id="76a82-106">Yeni bir Active Directory grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76a82-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="76a82-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76a82-107">EXAMPLES</span></span>

### <span data-ttu-id="76a82-108">Örnek 1-yeni bir AD grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="76a82-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="76a82-109">"MyGroupDisplayName" adlı yeni bir AD grubu ve "MyGroupNick" adres takma adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76a82-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="76a82-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76a82-110">PARAMETERS</span></span>

### <span data-ttu-id="76a82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a82-111">-DefaultProfile</span></span>
<span data-ttu-id="76a82-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76a82-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76a82-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="76a82-113">-Description</span></span>
<span data-ttu-id="76a82-114">Grubun açıklaması.</span><span class="sxs-lookup"><span data-stu-id="76a82-114">The description for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a82-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="76a82-115">-DisplayName</span></span>
<span data-ttu-id="76a82-116">Grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="76a82-116">The display name for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a82-117">-Posta takma adı</span><span class="sxs-lookup"><span data-stu-id="76a82-117">-MailNickname</span></span>
<span data-ttu-id="76a82-118">Grubun posta takma adı.</span><span class="sxs-lookup"><span data-stu-id="76a82-118">The mail nickname for the group.</span></span> <span data-ttu-id="76a82-119">@ İşaretini içeremez.</span><span class="sxs-lookup"><span data-stu-id="76a82-119">Cannot contain the @ sign.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a82-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="76a82-120">-Confirm</span></span>
<span data-ttu-id="76a82-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="76a82-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a82-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76a82-122">-WhatIf</span></span>
<span data-ttu-id="76a82-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="76a82-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76a82-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="76a82-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a82-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a82-125">CommonParameters</span></span>
<span data-ttu-id="76a82-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76a82-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a82-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="76a82-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a82-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76a82-128">INPUTS</span></span>

### <span data-ttu-id="76a82-129">System. String</span><span class="sxs-lookup"><span data-stu-id="76a82-129">System.String</span></span>

## <span data-ttu-id="76a82-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76a82-130">OUTPUTS</span></span>

### <span data-ttu-id="76a82-131">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="76a82-131">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="76a82-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76a82-132">NOTES</span></span>

## <span data-ttu-id="76a82-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76a82-133">RELATED LINKS</span></span>
