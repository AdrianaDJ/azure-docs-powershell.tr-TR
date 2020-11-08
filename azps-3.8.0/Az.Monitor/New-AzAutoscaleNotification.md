---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 010698183dec206002c0966fb8f37d629d24794a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098461"
---
# <span data-ttu-id="4931e-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="4931e-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="4931e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4931e-102">SYNOPSIS</span></span>
<span data-ttu-id="4931e-103">Otomatik ölçeklendirme e-posta bildirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4931e-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="4931e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4931e-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4931e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4931e-105">DESCRIPTION</span></span>
<span data-ttu-id="4931e-106">**Yeni-AzAutoscaleNotification** cmdlet 'ı otomatik ölçeklendirme için bir e-posta bildirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4931e-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="4931e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4931e-107">EXAMPLES</span></span>

### <span data-ttu-id="4931e-108">Örnek 1: otomatik ölçeklendirme e-posta bildirimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4931e-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="4931e-109">Bu komut belirtilen iki adres için otomatik bir e-posta bildirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4931e-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="4931e-110">Örnek 2: Abonelik Yöneticisi için otomatik ölçeklendirme e-posta bildirimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4931e-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="4931e-111">Bu komut, abonelik Yöneticisi için otomatik bir e-posta bildirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4931e-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="4931e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4931e-112">PARAMETERS</span></span>

### <span data-ttu-id="4931e-113">-Customeposta</span><span class="sxs-lookup"><span data-stu-id="4931e-113">-CustomEmail</span></span>
<span data-ttu-id="4931e-114">Virgülle ayrılmış e-posta adresleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4931e-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="4931e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4931e-115">-DefaultProfile</span></span>
<span data-ttu-id="4931e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4931e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4931e-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="4931e-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="4931e-118">Bu işlemin abonelik yöneticisine bir e-posta bildirimi gönderdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4931e-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="4931e-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="4931e-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="4931e-120">Bu işlemin ortak yöneticilere bir e-posta bildirimi gönderdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4931e-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="4931e-121">-Web kancası</span><span class="sxs-lookup"><span data-stu-id="4931e-121">-Webhook</span></span>
<span data-ttu-id="4931e-122">Otomatik ölçeklendirme Web kancaları için virgülle ayrılmış bir liste belirtir.</span><span class="sxs-lookup"><span data-stu-id="4931e-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="4931e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4931e-123">CommonParameters</span></span>
<span data-ttu-id="4931e-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4931e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4931e-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4931e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4931e-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4931e-126">INPUTS</span></span>

### <span data-ttu-id="4931e-127">Microsoft. Azure. Management. Monitor. Management. modeller. Web, Notification []</span><span class="sxs-lookup"><span data-stu-id="4931e-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="4931e-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="4931e-128">System.String[]</span></span>

### <span data-ttu-id="4931e-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4931e-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4931e-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4931e-130">OUTPUTS</span></span>

### <span data-ttu-id="4931e-131">Microsoft. Azure. Management. Monitor. Management. modeller. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="4931e-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="4931e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4931e-132">NOTES</span></span>

## <span data-ttu-id="4931e-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4931e-133">RELATED LINKS</span></span>

[<span data-ttu-id="4931e-134">Yeni-Azautoscaleweb kancası</span><span class="sxs-lookup"><span data-stu-id="4931e-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)

