---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: b5bc2f2eb99a8256dcaa6bc4f026d922f0f563ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936415"
---
# <span data-ttu-id="81221-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="81221-101">New-AzADGroup</span></span>

## <span data-ttu-id="81221-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81221-102">SYNOPSIS</span></span>
<span data-ttu-id="81221-103">Yeni bir Active Directory grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="81221-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="81221-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81221-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81221-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="81221-105">DESCRIPTION</span></span>
<span data-ttu-id="81221-106">Yeni bir Active Directory grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="81221-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="81221-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81221-107">EXAMPLES</span></span>

### <span data-ttu-id="81221-108">Örnek 1-yeni bir AD grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="81221-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "myemail@domain.com"
```

<span data-ttu-id="81221-109">"MyGroupDisplayName" ve posta takma adı "" adlı yeni bir AD grubu oluşturur myemail@domain.com .</span><span class="sxs-lookup"><span data-stu-id="81221-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "myemail@domain.com".</span></span>

## <span data-ttu-id="81221-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81221-110">PARAMETERS</span></span>

### <span data-ttu-id="81221-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81221-111">-DefaultProfile</span></span>
<span data-ttu-id="81221-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="81221-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81221-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="81221-113">-DisplayName</span></span>
<span data-ttu-id="81221-114">Grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="81221-114">The display name for the group.</span></span>

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

### <span data-ttu-id="81221-115">-Posta takma adı</span><span class="sxs-lookup"><span data-stu-id="81221-115">-MailNickname</span></span>
<span data-ttu-id="81221-116">Grubun posta takma adı.</span><span class="sxs-lookup"><span data-stu-id="81221-116">The mail nickname for the group.</span></span>

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

### <span data-ttu-id="81221-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="81221-117">-Confirm</span></span>
<span data-ttu-id="81221-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="81221-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81221-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81221-119">-WhatIf</span></span>
<span data-ttu-id="81221-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="81221-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81221-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="81221-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81221-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81221-122">CommonParameters</span></span>
<span data-ttu-id="81221-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81221-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81221-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81221-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81221-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81221-125">INPUTS</span></span>

### <span data-ttu-id="81221-126">System. String</span><span class="sxs-lookup"><span data-stu-id="81221-126">System.String</span></span>

## <span data-ttu-id="81221-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81221-127">OUTPUTS</span></span>

### <span data-ttu-id="81221-128">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="81221-128">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="81221-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81221-129">NOTES</span></span>

## <span data-ttu-id="81221-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81221-130">RELATED LINKS</span></span>
