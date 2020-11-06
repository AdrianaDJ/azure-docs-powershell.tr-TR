---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
ms.openlocfilehash: 85479695efee536aac054751fdd5a48d4b5de5ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592208"
---
# <span data-ttu-id="e3553-101">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="e3553-101">New-AzureRmAlertRuleEmail</span></span>

## <span data-ttu-id="e3553-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3553-102">SYNOPSIS</span></span>
<span data-ttu-id="e3553-103">Uyarı kuralı için e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3553-103">Creates an email action for an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3553-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3553-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleEmail [[-CustomEmails] <String[]>] [-SendToServiceOwners]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3553-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3553-105">DESCRIPTION</span></span>
<span data-ttu-id="e3553-106">**Yeni-AzureRmAlertRuleEmail** cmdlet 'i, bir uyarı kuralı için e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3553-106">The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="e3553-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3553-107">EXAMPLES</span></span>

### <span data-ttu-id="e3553-108">Örnek 1: hizmet sahipleri için bir uyarı kuralı e-posta eylemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e3553-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="e3553-109">Bu komut, bir uyarı kuralı başlatıldığında hizmet sahipleri için gönderilecek bir uyarı kuralı e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3553-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="e3553-110">Örnek 2: hizmet dışı sahipler için uyarı kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="e3553-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="e3553-111">Bu komut belirtilen e-posta adresleri için bir uyarı kuralı e-posta eylemi oluşturur, ancak hizmet sahipleri için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="e3553-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="e3553-112">Örnek 3: hizmet sahipleri ve hizmet dışı sahipler için bir uyarı kuralı e-posta eylemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e3553-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.net" -SendToServiceOwners
```

<span data-ttu-id="e3553-113">Bu komut, belirtilen adres ve hizmet sahipleri için bir uyarı kuralı e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3553-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="e3553-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3553-114">PARAMETERS</span></span>

### <span data-ttu-id="e3553-115">-Customepostaları</span><span class="sxs-lookup"><span data-stu-id="e3553-115">-CustomEmails</span></span>
<span data-ttu-id="e3553-116">Virgülle ayrılmış e-posta adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3553-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="e3553-117">-SendToServiceOwners</span><span class="sxs-lookup"><span data-stu-id="e3553-117">-SendToServiceOwners</span></span>
<span data-ttu-id="e3553-118">Bu işlemin, kural tetiklendiğinde hizmet sahiplerine e-posta gönderdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3553-118">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="e3553-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3553-119">-DefaultProfile</span></span>
<span data-ttu-id="e3553-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e3553-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3553-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3553-121">CommonParameters</span></span>
<span data-ttu-id="e3553-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3553-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3553-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3553-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3553-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3553-124">INPUTS</span></span>

## <span data-ttu-id="e3553-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3553-125">OUTPUTS</span></span>

### <span data-ttu-id="e3553-126">Microsoft. Azure. Management. Monitor. Management. modeller. Ruleemailate</span><span class="sxs-lookup"><span data-stu-id="e3553-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="e3553-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3553-127">NOTES</span></span>

## <span data-ttu-id="e3553-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3553-128">RELATED LINKS</span></span>

[<span data-ttu-id="e3553-129">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="e3553-129">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="e3553-130">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="e3553-130">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="e3553-131">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e3553-131">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="e3553-132">Yeni-Azurermalertruleweb kancası</span><span class="sxs-lookup"><span data-stu-id="e3553-132">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


