---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: ee95455b5081105ec4e28a4811e46ca92bfbc240
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590473"
---
# <span data-ttu-id="0c5bc-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="0c5bc-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="0c5bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c5bc-102">SYNOPSIS</span></span>
<span data-ttu-id="0c5bc-103">Otomatik ölçeklendirme e-posta bildirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c5bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c5bc-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator] 
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c5bc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c5bc-105">DESCRIPTION</span></span>
<span data-ttu-id="0c5bc-106">**Yeni-AzureRmAutoscaleNotification** cmdlet 'ı otomatik ölçeklendirme için bir e-posta bildirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="0c5bc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c5bc-107">EXAMPLES</span></span>

### <span data-ttu-id="0c5bc-108">Örnek 1: otomatik ölçeklendirme e-posta bildirimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0c5bc-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="0c5bc-109">Bu komut belirtilen iki adres için otomatik bir e-posta bildirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="0c5bc-110">Örnek 2: Abonelik Yöneticisi için otomatik ölçeklendirme e-posta bildirimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0c5bc-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="0c5bc-111">Bu komut, abonelik Yöneticisi için otomatik bir e-posta bildirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="0c5bc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c5bc-112">PARAMETERS</span></span>

### <span data-ttu-id="0c5bc-113">-Customeposta</span><span class="sxs-lookup"><span data-stu-id="0c5bc-113">-CustomEmail</span></span>
<span data-ttu-id="0c5bc-114">Virgülle ayrılmış e-posta adresleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-114">Specifies a comma-separated list of email addresses.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CustomEmails

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c5bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c5bc-115">-DefaultProfile</span></span>
<span data-ttu-id="0c5bc-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0c5bc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c5bc-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="0c5bc-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="0c5bc-118">Bu işlemin abonelik yöneticisine bir e-posta bildirimi gönderdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c5bc-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="0c5bc-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="0c5bc-120">Bu işlemin ortak yöneticilere bir e-posta bildirimi gönderdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: SendEmailToSubscriptionCoAdministrators

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c5bc-121">-Web kancası</span><span class="sxs-lookup"><span data-stu-id="0c5bc-121">-Webhook</span></span>
<span data-ttu-id="0c5bc-122">Otomatik ölçeklendirme Web kancaları için virgülle ayrılmış bir liste belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

```yaml
Type: WebhookNotification[]
Parameter Sets: (All)
Aliases: Webhooks

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c5bc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c5bc-123">CommonParameters</span></span>
<span data-ttu-id="0c5bc-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c5bc-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c5bc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c5bc-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c5bc-126">INPUTS</span></span>

### <span data-ttu-id="0c5bc-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0c5bc-127">None</span></span>
<span data-ttu-id="0c5bc-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0c5bc-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c5bc-129">OUTPUTS</span></span>

### <span data-ttu-id="0c5bc-130">Microsoft. Azure. Management. Monitor. Management. modeller. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="0c5bc-130">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="0c5bc-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c5bc-131">NOTES</span></span>

## <span data-ttu-id="0c5bc-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c5bc-132">RELATED LINKS</span></span>

[<span data-ttu-id="0c5bc-133">Yeni-Azurermautoscaleweb kancası</span><span class="sxs-lookup"><span data-stu-id="0c5bc-133">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


