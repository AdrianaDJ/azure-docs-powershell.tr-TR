---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 98d87c060c51d19db45e907f88d39f27350248c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322846"
---
# <span data-ttu-id="3b9d9-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="3b9d9-101">New-AzADGroup</span></span>

## <span data-ttu-id="3b9d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b9d9-102">SYNOPSIS</span></span>
<span data-ttu-id="3b9d9-103">Yeni bir Active Directory grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3b9d9-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="3b9d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b9d9-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b9d9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b9d9-105">DESCRIPTION</span></span>
<span data-ttu-id="3b9d9-106">Yeni bir Active Directory grubu oluşturur. Gerekli izinler aşağıdadır:</span><span class="sxs-lookup"><span data-stu-id="3b9d9-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="3b9d9-107">Azure Active Directory grafiği</span><span class="sxs-lookup"><span data-stu-id="3b9d9-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="3b9d9-108">Dizin. ReadWrite. tümü</span><span class="sxs-lookup"><span data-stu-id="3b9d9-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="3b9d9-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="3b9d9-109">Microsoft Graph</span></span>
  - <span data-ttu-id="3b9d9-110">Dizin. ReadWrite. tümü</span><span class="sxs-lookup"><span data-stu-id="3b9d9-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="3b9d9-111">PrivilegedAccess. ReadWrite. AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="3b9d9-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="3b9d9-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b9d9-112">EXAMPLES</span></span>

### <span data-ttu-id="3b9d9-113">Örnek 1: yeni bir AD grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="3b9d9-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="3b9d9-114">"MyGroupDisplayName" adlı yeni bir AD grubu ve "MyGroupNick" adres takma adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3b9d9-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="3b9d9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b9d9-115">PARAMETERS</span></span>

### <span data-ttu-id="3b9d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b9d9-116">-DefaultProfile</span></span>
<span data-ttu-id="3b9d9-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b9d9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b9d9-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="3b9d9-118">-Description</span></span>
<span data-ttu-id="3b9d9-119">Grubun açıklaması.</span><span class="sxs-lookup"><span data-stu-id="3b9d9-119">The description for the group.</span></span>

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

### <span data-ttu-id="3b9d9-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3b9d9-120">-DisplayName</span></span>
<span data-ttu-id="3b9d9-121">Grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="3b9d9-121">The display name for the group.</span></span>

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

### <span data-ttu-id="3b9d9-122">-Posta takma adı</span><span class="sxs-lookup"><span data-stu-id="3b9d9-122">-MailNickname</span></span>
<span data-ttu-id="3b9d9-123">Grubun posta takma adı.</span><span class="sxs-lookup"><span data-stu-id="3b9d9-123">The mail nickname for the group.</span></span> <span data-ttu-id="3b9d9-124">@ İşaretini içeremez.</span><span class="sxs-lookup"><span data-stu-id="3b9d9-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="3b9d9-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="3b9d9-125">-Confirm</span></span>
<span data-ttu-id="3b9d9-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3b9d9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b9d9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b9d9-127">-WhatIf</span></span>
<span data-ttu-id="3b9d9-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3b9d9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b9d9-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3b9d9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b9d9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b9d9-130">CommonParameters</span></span>
<span data-ttu-id="3b9d9-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b9d9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b9d9-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3b9d9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b9d9-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b9d9-133">INPUTS</span></span>

### <span data-ttu-id="3b9d9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3b9d9-134">System.String</span></span>

## <span data-ttu-id="3b9d9-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b9d9-135">OUTPUTS</span></span>

### <span data-ttu-id="3b9d9-136">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="3b9d9-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="3b9d9-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b9d9-137">NOTES</span></span>

## <span data-ttu-id="3b9d9-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b9d9-138">RELATED LINKS</span></span>
