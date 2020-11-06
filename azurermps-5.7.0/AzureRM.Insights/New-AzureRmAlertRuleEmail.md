---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
ms.openlocfilehash: b3484b410ef885567010c05660590808f3995308
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590476"
---
# <span data-ttu-id="f7a65-101">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="f7a65-101">New-AzureRmAlertRuleEmail</span></span>

## <span data-ttu-id="f7a65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7a65-102">SYNOPSIS</span></span>
<span data-ttu-id="f7a65-103">Uyarı kuralı için e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f7a65-103">Creates an email action for an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7a65-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7a65-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7a65-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7a65-105">DESCRIPTION</span></span>
<span data-ttu-id="f7a65-106">**Yeni-AzureRmAlertRuleEmail** cmdlet 'i, bir uyarı kuralı için e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f7a65-106">The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="f7a65-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7a65-107">EXAMPLES</span></span>

### <span data-ttu-id="f7a65-108">Örnek 1: hizmet sahipleri için bir uyarı kuralı e-posta eylemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="f7a65-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="f7a65-109">Bu komut, bir uyarı kuralı başlatıldığında hizmet sahipleri için gönderilecek bir uyarı kuralı e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f7a65-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="f7a65-110">Örnek 2: hizmet dışı sahipler için uyarı kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="f7a65-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="f7a65-111">Bu komut belirtilen e-posta adresleri için bir uyarı kuralı e-posta eylemi oluşturur, ancak hizmet sahipleri için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="f7a65-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="f7a65-112">Örnek 3: hizmet sahipleri ve hizmet dışı sahipler için bir uyarı kuralı e-posta eylemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="f7a65-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="f7a65-113">Bu komut, belirtilen adres ve hizmet sahipleri için bir uyarı kuralı e-posta eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f7a65-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="f7a65-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7a65-114">PARAMETERS</span></span>

### <span data-ttu-id="f7a65-115">-Customeposta</span><span class="sxs-lookup"><span data-stu-id="f7a65-115">-CustomEmail</span></span>
<span data-ttu-id="f7a65-116">Virgülle ayrılmış e-posta adreslerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7a65-116">Specifies a list of comma-separated e-mail addresses.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CustomEmails

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7a65-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7a65-117">-DefaultProfile</span></span>
<span data-ttu-id="f7a65-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f7a65-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7a65-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="f7a65-119">-SendToServiceOwner</span></span>
<span data-ttu-id="f7a65-120">Bu işlemin, kural tetiklendiğinde hizmet sahiplerine e-posta gönderdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7a65-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: SendToServiceOwners

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7a65-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7a65-121">CommonParameters</span></span>
<span data-ttu-id="f7a65-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7a65-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7a65-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7a65-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7a65-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7a65-124">INPUTS</span></span>

### <span data-ttu-id="f7a65-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f7a65-125">None</span></span>
<span data-ttu-id="f7a65-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f7a65-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7a65-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7a65-127">OUTPUTS</span></span>

### <span data-ttu-id="f7a65-128">Microsoft. Azure. Management. Monitor. Management. modeller. Ruleemailate</span><span class="sxs-lookup"><span data-stu-id="f7a65-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="f7a65-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7a65-129">NOTES</span></span>

## <span data-ttu-id="f7a65-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7a65-130">RELATED LINKS</span></span>

[<span data-ttu-id="f7a65-131">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="f7a65-131">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="f7a65-132">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="f7a65-132">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="f7a65-133">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="f7a65-133">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="f7a65-134">Yeni-Azurermalertruleweb kancası</span><span class="sxs-lookup"><span data-stu-id="f7a65-134">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


