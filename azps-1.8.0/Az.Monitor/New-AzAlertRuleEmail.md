---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: cfdd18a02a5e0507e86a37dee1e1662bb5094f37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915635"
---
# <span data-ttu-id="f1de8-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="f1de8-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="f1de8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1de8-102">SYNOPSIS</span></span>
<span data-ttu-id="f1de8-103">Uyarı kuralı için e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1de8-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="f1de8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1de8-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1de8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1de8-105">DESCRIPTION</span></span>
<span data-ttu-id="f1de8-106">**Yeni-AzAlertRuleEmail** cmdlet 'i, bir uyarı kuralı için e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1de8-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="f1de8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1de8-107">EXAMPLES</span></span>

### <span data-ttu-id="f1de8-108">Örnek 1: hizmet sahipleri için bir uyarı kuralı e-posta eylemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="f1de8-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="f1de8-109">Bu komut, bir uyarı kuralı başlatıldığında hizmet sahipleri için gönderilecek bir uyarı kuralı e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1de8-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="f1de8-110">Örnek 2: hizmet dışı sahipler için uyarı kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="f1de8-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="f1de8-111">Bu komut belirtilen e-posta adresleri için bir uyarı kuralı e-posta eylemi oluşturur, ancak hizmet sahipleri için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="f1de8-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="f1de8-112">Örnek 3: hizmet sahipleri ve hizmet dışı sahipler için bir uyarı kuralı e-posta eylemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="f1de8-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="f1de8-113">Bu komut, belirtilen adres ve hizmet sahipleri için bir uyarı kuralı e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1de8-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="f1de8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1de8-114">PARAMETERS</span></span>

### <span data-ttu-id="f1de8-115">-Customeposta</span><span class="sxs-lookup"><span data-stu-id="f1de8-115">-CustomEmail</span></span>
<span data-ttu-id="f1de8-116">Virgülle ayrılmış e-posta adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1de8-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="f1de8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1de8-117">-DefaultProfile</span></span>
<span data-ttu-id="f1de8-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f1de8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1de8-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="f1de8-119">-SendToServiceOwner</span></span>
<span data-ttu-id="f1de8-120">Bu işlemin, kural tetiklendiğinde hizmet sahiplerine e-posta gönderdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f1de8-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="f1de8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1de8-121">CommonParameters</span></span>
<span data-ttu-id="f1de8-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1de8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1de8-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1de8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1de8-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1de8-124">INPUTS</span></span>

### <span data-ttu-id="f1de8-125">System. String []</span><span class="sxs-lookup"><span data-stu-id="f1de8-125">System.String[]</span></span>

### <span data-ttu-id="f1de8-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f1de8-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f1de8-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1de8-127">OUTPUTS</span></span>

### <span data-ttu-id="f1de8-128">Microsoft. Azure. Management. Monitor. Management. modeller. Ruleemailate</span><span class="sxs-lookup"><span data-stu-id="f1de8-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="f1de8-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1de8-129">NOTES</span></span>

## <span data-ttu-id="f1de8-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1de8-130">RELATED LINKS</span></span>

[<span data-ttu-id="f1de8-131">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="f1de8-131">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="f1de8-132">Add-Azmetrik ıalertrule</span><span class="sxs-lookup"><span data-stu-id="f1de8-132">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="f1de8-133">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="f1de8-133">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="f1de8-134">Yeni-Azalertruleweb kancası</span><span class="sxs-lookup"><span data-stu-id="f1de8-134">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)

