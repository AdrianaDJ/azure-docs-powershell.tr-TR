---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertruleemail
schema: 2.0.0
ms.openlocfilehash: 20134cc0f2eef927361439fb431bc4ab9308a9a1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940136"
---
# <span data-ttu-id="0a7d1-101">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="0a7d1-101">New-AzureRmAlertRuleEmail</span></span>

## <span data-ttu-id="0a7d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a7d1-102">SYNOPSIS</span></span>
<span data-ttu-id="0a7d1-103">Uyarı kuralı için e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0a7d1-103">Creates an email action for an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a7d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a7d1-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a7d1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a7d1-105">DESCRIPTION</span></span>
<span data-ttu-id="0a7d1-106">**Yeni-AzureRmAlertRuleEmail** cmdlet 'i, bir uyarı kuralı için e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0a7d1-106">The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="0a7d1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a7d1-107">EXAMPLES</span></span>

### <span data-ttu-id="0a7d1-108">Örnek 1: hizmet sahipleri için bir uyarı kuralı e-posta eylemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0a7d1-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="0a7d1-109">Bu komut, bir uyarı kuralı başlatıldığında hizmet sahipleri için gönderilecek bir uyarı kuralı e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0a7d1-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="0a7d1-110">Örnek 2: hizmet dışı sahipler için uyarı kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="0a7d1-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="0a7d1-111">Bu komut belirtilen e-posta adresleri için bir uyarı kuralı e-posta eylemi oluşturur, ancak hizmet sahipleri için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="0a7d1-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="0a7d1-112">Örnek 3: hizmet sahipleri ve hizmet dışı sahipler için bir uyarı kuralı e-posta eylemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0a7d1-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="0a7d1-113">Bu komut, belirtilen adres ve hizmet sahipleri için bir uyarı kuralı e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0a7d1-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="0a7d1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a7d1-114">PARAMETERS</span></span>

### <span data-ttu-id="0a7d1-115">-Customeposta</span><span class="sxs-lookup"><span data-stu-id="0a7d1-115">-CustomEmail</span></span>
<span data-ttu-id="0a7d1-116">Virgülle ayrılmış e-posta adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a7d1-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="0a7d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a7d1-117">-DefaultProfile</span></span>
<span data-ttu-id="0a7d1-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0a7d1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a7d1-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="0a7d1-119">-SendToServiceOwner</span></span>
<span data-ttu-id="0a7d1-120">Bu işlemin, kural tetiklendiğinde hizmet sahiplerine e-posta gönderdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a7d1-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="0a7d1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a7d1-121">CommonParameters</span></span>
<span data-ttu-id="0a7d1-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a7d1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a7d1-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a7d1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a7d1-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a7d1-124">INPUTS</span></span>

### <span data-ttu-id="0a7d1-125">System. String []</span><span class="sxs-lookup"><span data-stu-id="0a7d1-125">System.String[]</span></span>

### <span data-ttu-id="0a7d1-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0a7d1-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0a7d1-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a7d1-127">OUTPUTS</span></span>

### <span data-ttu-id="0a7d1-128">Microsoft. Azure. Management. Monitor. Management. modeller. Ruleemailate</span><span class="sxs-lookup"><span data-stu-id="0a7d1-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="0a7d1-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a7d1-129">NOTES</span></span>

## <span data-ttu-id="0a7d1-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a7d1-130">RELATED LINKS</span></span>



[<span data-ttu-id="0a7d1-131">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="0a7d1-131">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="0a7d1-132">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="0a7d1-132">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="0a7d1-133">Yeni-Azurermalertruleweb kancası</span><span class="sxs-lookup"><span data-stu-id="0a7d1-133">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


