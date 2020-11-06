---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: f6791d2cc962f0bb0db038ad8c5391425c09bfbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594277"
---
# <span data-ttu-id="26b29-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="26b29-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="26b29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26b29-102">SYNOPSIS</span></span>
<span data-ttu-id="26b29-103">Otomatik ölçeklendirme e-posta bildirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="26b29-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26b29-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26b29-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhooks] <WebhookNotification[]>] [[-CustomEmails] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26b29-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="26b29-105">DESCRIPTION</span></span>
<span data-ttu-id="26b29-106">**Yeni-AzureRmAutoscaleNotification** cmdlet 'ı otomatik ölçeklendirme için bir e-posta bildirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="26b29-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="26b29-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26b29-107">EXAMPLES</span></span>

### <span data-ttu-id="26b29-108">Örnek 1: otomatik ölçeklendirme e-posta bildirimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="26b29-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="26b29-109">Bu komut belirtilen iki adres için otomatik bir e-posta bildirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="26b29-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="26b29-110">Örnek 2: Abonelik Yöneticisi için otomatik ölçeklendirme e-posta bildirimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="26b29-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="26b29-111">Bu komut, abonelik Yöneticisi için otomatik bir e-posta bildirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="26b29-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="26b29-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26b29-112">PARAMETERS</span></span>

### <span data-ttu-id="26b29-113">-Customepostaları</span><span class="sxs-lookup"><span data-stu-id="26b29-113">-CustomEmails</span></span>
<span data-ttu-id="26b29-114">Virgülle ayrılmış e-posta adresleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="26b29-114">Specifies a comma-separated list of email addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b29-115">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="26b29-115">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="26b29-116">Bu işlemin abonelik yöneticisine bir e-posta bildirimi gönderdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="26b29-116">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="26b29-117">-SendEmailToSubscriptionCoAdministrators</span><span class="sxs-lookup"><span data-stu-id="26b29-117">-SendEmailToSubscriptionCoAdministrators</span></span>
<span data-ttu-id="26b29-118">Bu işlemin ortak yöneticilere bir e-posta bildirimi gönderdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="26b29-118">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="26b29-119">-Web kancaları</span><span class="sxs-lookup"><span data-stu-id="26b29-119">-Webhooks</span></span>
<span data-ttu-id="26b29-120">Otomatik ölçeklendirme Web kancaları için virgülle ayrılmış bir liste belirtir.</span><span class="sxs-lookup"><span data-stu-id="26b29-120">Specifies a comma-separated list of Autoscale webhooks.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b29-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b29-121">-DefaultProfile</span></span>
<span data-ttu-id="26b29-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="26b29-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26b29-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b29-123">CommonParameters</span></span>
<span data-ttu-id="26b29-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26b29-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b29-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26b29-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b29-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26b29-126">INPUTS</span></span>

## <span data-ttu-id="26b29-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26b29-127">OUTPUTS</span></span>

### <span data-ttu-id="26b29-128">Microsoft. Azure. Management. Monitor. Management. modeller. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="26b29-128">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="26b29-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26b29-129">NOTES</span></span>

## <span data-ttu-id="26b29-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26b29-130">RELATED LINKS</span></span>

[<span data-ttu-id="26b29-131">Yeni-Azurermautoscaleweb kancası</span><span class="sxs-lookup"><span data-stu-id="26b29-131">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


