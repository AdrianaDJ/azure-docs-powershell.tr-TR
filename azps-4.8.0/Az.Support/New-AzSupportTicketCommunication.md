---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 3a0191e1df223427ec7d60dfd92f7607e2c171b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267513"
---
# <span data-ttu-id="6cd81-101">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="6cd81-101">New-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="6cd81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cd81-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd81-103">Yeni bir destek bileti iletişimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6cd81-103">Creates a new support ticket communication.</span></span>

## <span data-ttu-id="6cd81-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6cd81-104">SYNTAX</span></span>

### <span data-ttu-id="6cd81-105">CreateByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6cd81-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6cd81-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cd81-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6cd81-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6cd81-107">DESCRIPTION</span></span>
<span data-ttu-id="6cd81-108">Azure destek biletini yeni bir müşteri iletişimi ekler.</span><span class="sxs-lookup"><span data-stu-id="6cd81-108">Adds a new customer communication to an Azure support ticket.</span></span>

## <span data-ttu-id="6cd81-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6cd81-109">EXAMPLES</span></span>

### <span data-ttu-id="6cd81-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6cd81-110">Example 1</span></span>
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## <span data-ttu-id="6cd81-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6cd81-111">PARAMETERS</span></span>

### <span data-ttu-id="6cd81-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="6cd81-112">-AsJob</span></span>
<span data-ttu-id="6cd81-113">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="6cd81-113">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cd81-114">-Gövde</span><span class="sxs-lookup"><span data-stu-id="6cd81-114">-Body</span></span>
<span data-ttu-id="6cd81-115">İletişimin gövdesi.</span><span class="sxs-lookup"><span data-stu-id="6cd81-115">Body of the communication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cd81-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cd81-116">-DefaultProfile</span></span>
<span data-ttu-id="6cd81-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6cd81-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cd81-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="6cd81-118">-Name</span></span>
<span data-ttu-id="6cd81-119">İletişim kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="6cd81-119">Name of the communication resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cd81-120">-Gönderen</span><span class="sxs-lookup"><span data-stu-id="6cd81-120">-Sender</span></span>
<span data-ttu-id="6cd81-121">Gönderenin e-posta adresi.</span><span class="sxs-lookup"><span data-stu-id="6cd81-121">Email address of the sender.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cd81-122">-Konu</span><span class="sxs-lookup"><span data-stu-id="6cd81-122">-Subject</span></span>
<span data-ttu-id="6cd81-123">İletişimin konusu.</span><span class="sxs-lookup"><span data-stu-id="6cd81-123">Subject of the communication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cd81-124">-Supportbilet adı</span><span class="sxs-lookup"><span data-stu-id="6cd81-124">-SupportTicketName</span></span>
<span data-ttu-id="6cd81-125">Destek bileti adı.</span><span class="sxs-lookup"><span data-stu-id="6cd81-125">Support ticket name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cd81-126">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="6cd81-126">-SupportTicketObject</span></span>
<span data-ttu-id="6cd81-127">Destek bileti nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6cd81-127">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cd81-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="6cd81-128">-Confirm</span></span>
<span data-ttu-id="6cd81-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6cd81-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cd81-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cd81-130">-WhatIf</span></span>
<span data-ttu-id="6cd81-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6cd81-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cd81-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6cd81-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cd81-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd81-133">CommonParameters</span></span>
<span data-ttu-id="6cd81-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6cd81-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd81-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6cd81-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd81-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6cd81-136">INPUTS</span></span>

### <span data-ttu-id="6cd81-137">Microsoft. Azure. Commands. support. model. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="6cd81-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="6cd81-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6cd81-138">OUTPUTS</span></span>

### <span data-ttu-id="6cd81-139">Microsoft. Azure. Commands. support. model. Pssupportfcommunication Iletişimi</span><span class="sxs-lookup"><span data-stu-id="6cd81-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="6cd81-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6cd81-140">NOTES</span></span>

## <span data-ttu-id="6cd81-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6cd81-141">RELATED LINKS</span></span>
