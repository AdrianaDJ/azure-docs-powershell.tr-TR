---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 3738e0d66c7dfb1a1aed56d5cfe8e1679e4e34e1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935724"
---
# <span data-ttu-id="c852c-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="c852c-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="c852c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c852c-102">SYNOPSIS</span></span>
<span data-ttu-id="c852c-103">Uyarı kuralı için e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c852c-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="c852c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c852c-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c852c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c852c-105">DESCRIPTION</span></span>
<span data-ttu-id="c852c-106">**Yeni-AzAlertRuleEmail** cmdlet 'i, bir uyarı kuralı için e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c852c-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="c852c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c852c-107">EXAMPLES</span></span>

### <span data-ttu-id="c852c-108">Örnek 1: hizmet sahipleri için bir uyarı kuralı e-posta eylemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c852c-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="c852c-109">Bu komut, bir uyarı kuralı başlatıldığında hizmet sahipleri için gönderilecek bir uyarı kuralı e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c852c-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="c852c-110">Örnek 2: hizmet dışı sahipler için uyarı kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="c852c-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="c852c-111">Bu komut belirtilen e-posta adresleri için bir uyarı kuralı e-posta eylemi oluşturur, ancak hizmet sahipleri için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="c852c-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="c852c-112">Örnek 3: hizmet sahipleri ve hizmet dışı sahipler için bir uyarı kuralı e-posta eylemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c852c-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="c852c-113">Bu komut, belirtilen adres ve hizmet sahipleri için bir uyarı kuralı e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c852c-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="c852c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c852c-114">PARAMETERS</span></span>

### <span data-ttu-id="c852c-115">-Customeposta</span><span class="sxs-lookup"><span data-stu-id="c852c-115">-CustomEmail</span></span>
<span data-ttu-id="c852c-116">Virgülle ayrılmış e-posta adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c852c-116">Specifies a list of comma-separated e-mail addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c852c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c852c-117">-DefaultProfile</span></span>
<span data-ttu-id="c852c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c852c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c852c-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="c852c-119">-SendToServiceOwner</span></span>
<span data-ttu-id="c852c-120">Bu işlemin, kural tetiklendiğinde hizmet sahiplerine e-posta gönderdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c852c-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c852c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c852c-121">CommonParameters</span></span>
<span data-ttu-id="c852c-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c852c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c852c-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c852c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c852c-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c852c-124">INPUTS</span></span>

### <span data-ttu-id="c852c-125">System. String []</span><span class="sxs-lookup"><span data-stu-id="c852c-125">System.String[]</span></span>

### <span data-ttu-id="c852c-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c852c-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c852c-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c852c-127">OUTPUTS</span></span>

### <span data-ttu-id="c852c-128">Microsoft. Azure. Management. Monitor. Management. modeller. Ruleemailate</span><span class="sxs-lookup"><span data-stu-id="c852c-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="c852c-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c852c-129">NOTES</span></span>

## <span data-ttu-id="c852c-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c852c-130">RELATED LINKS</span></span>

[<span data-ttu-id="c852c-131">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="c852c-131">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="c852c-132">Add-Azmetrik ıalertrule</span><span class="sxs-lookup"><span data-stu-id="c852c-132">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="c852c-133">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="c852c-133">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="c852c-134">Yeni-Azalertruleweb kancası</span><span class="sxs-lookup"><span data-stu-id="c852c-134">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


