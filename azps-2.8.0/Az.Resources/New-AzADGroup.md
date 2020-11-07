---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: d1a5057b25c08d1c93512ad3f439a9b4b208552f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932573"
---
# <span data-ttu-id="53ac9-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="53ac9-101">New-AzADGroup</span></span>

## <span data-ttu-id="53ac9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="53ac9-103">Yeni bir Active Directory grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="53ac9-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="53ac9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="53ac9-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <string>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53ac9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="53ac9-105">DESCRIPTION</span></span>
<span data-ttu-id="53ac9-106">Yeni bir Active Directory grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="53ac9-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="53ac9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="53ac9-107">EXAMPLES</span></span>

### <span data-ttu-id="53ac9-108">Örnek 1-yeni bir AD grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="53ac9-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="53ac9-109">"MyGroupDisplayName" adlı yeni bir AD grubu ve "MyGroupNick" adres takma adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="53ac9-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="53ac9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="53ac9-110">PARAMETERS</span></span>

### <span data-ttu-id="53ac9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53ac9-111">-DefaultProfile</span></span>
<span data-ttu-id="53ac9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="53ac9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53ac9-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="53ac9-113">-Description</span></span>
<span data-ttu-id="53ac9-114">Grubun açıklaması.</span><span class="sxs-lookup"><span data-stu-id="53ac9-114">The description for the group.</span></span>

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

### <span data-ttu-id="53ac9-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="53ac9-115">-DisplayName</span></span>
<span data-ttu-id="53ac9-116">Grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="53ac9-116">The display name for the group.</span></span>

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

### <span data-ttu-id="53ac9-117">-Posta takma adı</span><span class="sxs-lookup"><span data-stu-id="53ac9-117">-MailNickname</span></span>
<span data-ttu-id="53ac9-118">Grubun posta takma adı.</span><span class="sxs-lookup"><span data-stu-id="53ac9-118">The mail nickname for the group.</span></span> <span data-ttu-id="53ac9-119">@ İşaretini içeremez.</span><span class="sxs-lookup"><span data-stu-id="53ac9-119">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="53ac9-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="53ac9-120">-Confirm</span></span>
<span data-ttu-id="53ac9-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="53ac9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53ac9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53ac9-122">-WhatIf</span></span>
<span data-ttu-id="53ac9-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="53ac9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53ac9-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="53ac9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53ac9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53ac9-125">CommonParameters</span></span>
<span data-ttu-id="53ac9-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="53ac9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53ac9-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53ac9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53ac9-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="53ac9-128">INPUTS</span></span>

### <span data-ttu-id="53ac9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="53ac9-129">System.String</span></span>

## <span data-ttu-id="53ac9-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="53ac9-130">OUTPUTS</span></span>

### <span data-ttu-id="53ac9-131">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="53ac9-131">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="53ac9-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="53ac9-132">NOTES</span></span>

## <span data-ttu-id="53ac9-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="53ac9-133">RELATED LINKS</span></span>
