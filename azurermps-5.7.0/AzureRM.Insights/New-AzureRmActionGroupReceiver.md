---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
ms.openlocfilehash: 1c35572191ccf66bd7fd4e88e0996a8efdd1b82b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590480"
---
# <span data-ttu-id="4ed02-101">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="4ed02-101">New-AzureRmActionGroupReceiver</span></span>

## <span data-ttu-id="4ed02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ed02-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed02-103">Yeni bir eylem grubu alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4ed02-103">Creates an new action group receiver.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ed02-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ed02-104">SYNTAX</span></span>

### <span data-ttu-id="4ed02-105">Newemailalıcı(varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4ed02-105">NewEmailReceiver (Default)</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ed02-106">Newsmsalıcısı</span><span class="sxs-lookup"><span data-stu-id="4ed02-106">NewSmsReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ed02-107">Newwebalıcıalıcı</span><span class="sxs-lookup"><span data-stu-id="4ed02-107">NewWebhookReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ed02-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ed02-108">DESCRIPTION</span></span>
<span data-ttu-id="4ed02-109">**Yeni-Azurermactiongroupahize** cmdlet 'i bellekte yeni eylem grubu alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4ed02-109">The **New-AzureRmActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="4ed02-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ed02-110">EXAMPLES</span></span>

### <span data-ttu-id="4ed02-111">Örnek 1: bellekte yeni bir e-posta alıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4ed02-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzureRmActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="4ed02-112">Bu komut bellekte yeni bir e-posta alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4ed02-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="4ed02-113">Örnek 2: bellekte yeni bir SMS alıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4ed02-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzureRmActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="4ed02-114">Bu komut bellekte yeni bir SMS alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4ed02-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="4ed02-115">Örnek 3: bellekte yeni bir Web kancası alıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4ed02-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzureRmActionGroupReceiver -Name 'webhookReceiver1' -SMSReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="4ed02-116">Bu komut bellekte yeni bir Web kancası alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4ed02-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="4ed02-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ed02-117">PARAMETERS</span></span>

### <span data-ttu-id="4ed02-118">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="4ed02-118">-CountryCode</span></span>
<span data-ttu-id="4ed02-119">SMS alıcısının ülke kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ed02-119">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: String
Parameter Sets: NewSmsReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ed02-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed02-120">-DefaultProfile</span></span>
<span data-ttu-id="4ed02-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4ed02-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ed02-122">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="4ed02-122">-EmailAddress</span></span>
<span data-ttu-id="4ed02-123">E-posta alıcısının adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ed02-123">Specifies the address for the Email receiver.</span></span>

```yaml
Type: String
Parameter Sets: NewEmailReceiver
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ed02-124">-Emailahize</span><span class="sxs-lookup"><span data-stu-id="4ed02-124">-EmailReceiver</span></span>
<span data-ttu-id="4ed02-125">E-posta alıcısının oluşturulacağını belirtir</span><span class="sxs-lookup"><span data-stu-id="4ed02-125">Specifies to create an Email receiver</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ed02-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="4ed02-126">-Name</span></span>
<span data-ttu-id="4ed02-127">Alıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ed02-127">Specifies the name for the receiver.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ed02-128">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="4ed02-128">-PhoneNumber</span></span>
<span data-ttu-id="4ed02-129">SMS alıcısının telefon numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ed02-129">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: String
Parameter Sets: NewSmsReceiver
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ed02-130">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="4ed02-130">-ServiceUri</span></span>
<span data-ttu-id="4ed02-131">Web kancası alıcısının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ed02-131">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: String
Parameter Sets: NewWebhookReceiver
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ed02-132">-Smsahize</span><span class="sxs-lookup"><span data-stu-id="4ed02-132">-SmsReceiver</span></span>
<span data-ttu-id="4ed02-133">SMS alıcısı oluşturulacağını belirtir</span><span class="sxs-lookup"><span data-stu-id="4ed02-133">Specifies to create a SMS receiver</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ed02-134">-Webalıcıalıcı</span><span class="sxs-lookup"><span data-stu-id="4ed02-134">-WebhookReceiver</span></span>
<span data-ttu-id="4ed02-135">Web kancası alıcısının oluşturulacağını belirtir</span><span class="sxs-lookup"><span data-stu-id="4ed02-135">Specifies to create a webhook receiver</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ed02-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed02-136">CommonParameters</span></span>
<span data-ttu-id="4ed02-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ed02-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed02-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ed02-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed02-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ed02-139">INPUTS</span></span>

### <span data-ttu-id="4ed02-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4ed02-140">None</span></span>
<span data-ttu-id="4ed02-141">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4ed02-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4ed02-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ed02-142">OUTPUTS</span></span>

### <span data-ttu-id="4ed02-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="4ed02-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="4ed02-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ed02-144">NOTES</span></span>

## <span data-ttu-id="4ed02-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ed02-145">RELATED LINKS</span></span>

<span data-ttu-id="4ed02-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="4ed02-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span></span>
