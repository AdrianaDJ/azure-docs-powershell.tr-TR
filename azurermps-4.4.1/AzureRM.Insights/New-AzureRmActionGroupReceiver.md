---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
ms.openlocfilehash: cd08e0106fe78ddae04ac4543210b310fe3aa579
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763373"
---
# <span data-ttu-id="15e01-101">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="15e01-101">New-AzureRmActionGroupReceiver</span></span>

## <span data-ttu-id="15e01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15e01-102">SYNOPSIS</span></span>
<span data-ttu-id="15e01-103">Yeni bir eylem grubu alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15e01-103">Creates an new action group receiver.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15e01-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15e01-104">SYNTAX</span></span>

### <span data-ttu-id="15e01-105">Newemailalıcı(varsayılan)</span><span class="sxs-lookup"><span data-stu-id="15e01-105">NewEmailReceiver (Default)</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15e01-106">Newsmsalıcısı</span><span class="sxs-lookup"><span data-stu-id="15e01-106">NewSmsReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15e01-107">Newwebalıcıalıcı</span><span class="sxs-lookup"><span data-stu-id="15e01-107">NewWebhookReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15e01-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="15e01-108">DESCRIPTION</span></span>
<span data-ttu-id="15e01-109">**Yeni-Azurermactiongroupahize** cmdlet 'i bellekte yeni eylem grubu alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15e01-109">The **New-AzureRmActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="15e01-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15e01-110">EXAMPLES</span></span>

### <span data-ttu-id="15e01-111">Örnek 1: bellekte yeni bir e-posta alıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="15e01-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzureRmActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="15e01-112">Bu komut bellekte yeni bir e-posta alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15e01-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="15e01-113">Örnek 2: bellekte yeni bir SMS alıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="15e01-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzureRmActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="15e01-114">Bu komut bellekte yeni bir SMS alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15e01-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="15e01-115">Örnek 3: bellekte yeni bir Web kancası alıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="15e01-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzureRmActionGroupReceiver -Name 'webhookReceiver1' -SMSReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="15e01-116">Bu komut bellekte yeni bir Web kancası alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15e01-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="15e01-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15e01-117">PARAMETERS</span></span>

### <span data-ttu-id="15e01-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="15e01-118">-Name</span></span>
<span data-ttu-id="15e01-119">Alıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15e01-119">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="15e01-120">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="15e01-120">-EmailAddress</span></span>
<span data-ttu-id="15e01-121">E-posta alıcısının adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="15e01-121">Specifies the address for the Email receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewEmailReceiver
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e01-122">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="15e01-122">-CountryCode</span></span>
<span data-ttu-id="15e01-123">SMS alıcısının ülke kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="15e01-123">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e01-124">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="15e01-124">-PhoneNumber</span></span>
<span data-ttu-id="15e01-125">SMS alıcısının telefon numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15e01-125">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e01-126">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="15e01-126">-ServiceUri</span></span>
<span data-ttu-id="15e01-127">Web kancası alıcısının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="15e01-127">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e01-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15e01-128">-DefaultProfile</span></span>
<span data-ttu-id="15e01-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15e01-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15e01-130">-Emailahize</span><span class="sxs-lookup"><span data-stu-id="15e01-130">-EmailReceiver</span></span>
<span data-ttu-id="15e01-131">E-posta alıcısının oluşturulacağını belirtir</span><span class="sxs-lookup"><span data-stu-id="15e01-131">Specifies to create an Email receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e01-132">-Smsahize</span><span class="sxs-lookup"><span data-stu-id="15e01-132">-SmsReceiver</span></span>
<span data-ttu-id="15e01-133">SMS alıcısı oluşturulacağını belirtir</span><span class="sxs-lookup"><span data-stu-id="15e01-133">Specifies to create a SMS receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e01-134">-Webalıcıalıcı</span><span class="sxs-lookup"><span data-stu-id="15e01-134">-WebhookReceiver</span></span>
<span data-ttu-id="15e01-135">Web kancası alıcısının oluşturulacağını belirtir</span><span class="sxs-lookup"><span data-stu-id="15e01-135">Specifies to create a webhook receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e01-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15e01-136">CommonParameters</span></span>
<span data-ttu-id="15e01-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15e01-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15e01-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15e01-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15e01-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15e01-139">INPUTS</span></span>

## <span data-ttu-id="15e01-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15e01-140">OUTPUTS</span></span>

### <span data-ttu-id="15e01-141">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="15e01-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="15e01-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15e01-142">NOTES</span></span>

## <span data-ttu-id="15e01-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15e01-143">RELATED LINKS</span></span>

<span data-ttu-id="15e01-144">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="15e01-144">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span></span>
