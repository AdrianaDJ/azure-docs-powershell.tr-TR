---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadgroup
schema: 2.0.0
ms.openlocfilehash: fa9f708355e9c2fd4df530955db1d893e7591740
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939466"
---
# <span data-ttu-id="2f4eb-101">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="2f4eb-101">New-AzureRmADGroup</span></span>

## <span data-ttu-id="2f4eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f4eb-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4eb-103">Yeni bir Active Directory grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2f4eb-103">Creates a new active directory group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f4eb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f4eb-104">SYNTAX</span></span>

```
New-AzureRmADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f4eb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f4eb-105">DESCRIPTION</span></span>
<span data-ttu-id="2f4eb-106">Yeni bir Active Directory grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2f4eb-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="2f4eb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f4eb-107">EXAMPLES</span></span>

### <span data-ttu-id="2f4eb-108">Örnek 1-yeni bir AD grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="2f4eb-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzureRmADGroup -DisplayName "MyGroupDisplayName" -MailNickname "myemail@domain.com"
```

<span data-ttu-id="2f4eb-109">"MyGroupDisplayName" ve posta takma adı "" adlı yeni bir AD grubu oluşturur myemail@domain.com .</span><span class="sxs-lookup"><span data-stu-id="2f4eb-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "myemail@domain.com".</span></span>

## <span data-ttu-id="2f4eb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f4eb-110">PARAMETERS</span></span>

### <span data-ttu-id="2f4eb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f4eb-111">-DefaultProfile</span></span>
<span data-ttu-id="2f4eb-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2f4eb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4eb-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2f4eb-113">-DisplayName</span></span>
<span data-ttu-id="2f4eb-114">Grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="2f4eb-114">The display name for the group.</span></span>

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

### <span data-ttu-id="2f4eb-115">-Posta takma adı</span><span class="sxs-lookup"><span data-stu-id="2f4eb-115">-MailNickname</span></span>
<span data-ttu-id="2f4eb-116">Grubun posta takma adı.</span><span class="sxs-lookup"><span data-stu-id="2f4eb-116">The mail nickname for the group.</span></span>

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

### <span data-ttu-id="2f4eb-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="2f4eb-117">-Confirm</span></span>
<span data-ttu-id="2f4eb-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2f4eb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f4eb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f4eb-119">-WhatIf</span></span>
<span data-ttu-id="2f4eb-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2f4eb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f4eb-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2f4eb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f4eb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4eb-122">CommonParameters</span></span>
<span data-ttu-id="2f4eb-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f4eb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4eb-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f4eb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4eb-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f4eb-125">INPUTS</span></span>

### <span data-ttu-id="2f4eb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2f4eb-126">System.String</span></span>

## <span data-ttu-id="2f4eb-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f4eb-127">OUTPUTS</span></span>

### <span data-ttu-id="2f4eb-128">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="2f4eb-128">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="2f4eb-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f4eb-129">NOTES</span></span>

## <span data-ttu-id="2f4eb-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f4eb-130">RELATED LINKS</span></span>
