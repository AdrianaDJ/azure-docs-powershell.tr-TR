---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: 35f540d26464b7cdc4b08916f1397b71ee7cca18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915644"
---
# <span data-ttu-id="d7b01-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="d7b01-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="d7b01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7b01-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b01-103">Yeni bir eylem grubu alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7b01-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="d7b01-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7b01-104">SYNTAX</span></span>

### <span data-ttu-id="d7b01-105">Newemailalıcı(varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d7b01-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7b01-106">Newsmsalıcısı</span><span class="sxs-lookup"><span data-stu-id="d7b01-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7b01-107">Newwebalıcıalıcı</span><span class="sxs-lookup"><span data-stu-id="d7b01-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7b01-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7b01-108">DESCRIPTION</span></span>
<span data-ttu-id="d7b01-109">**Yeni-Azactiongroupahize** cmdlet 'i bellekte yeni eylem grubu alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7b01-109">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="d7b01-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7b01-110">EXAMPLES</span></span>

### <span data-ttu-id="d7b01-111">Örnek 1: bellekte yeni bir e-posta alıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d7b01-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="d7b01-112">Bu komut bellekte yeni bir e-posta alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7b01-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="d7b01-113">Örnek 2: bellekte yeni bir SMS alıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d7b01-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="d7b01-114">Bu komut bellekte yeni bir SMS alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7b01-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="d7b01-115">Örnek 3: bellekte yeni bir Web kancası alıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d7b01-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="d7b01-116">Bu komut bellekte yeni bir Web kancası alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7b01-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="d7b01-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7b01-117">PARAMETERS</span></span>

### <span data-ttu-id="d7b01-118">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="d7b01-118">-CountryCode</span></span>
<span data-ttu-id="d7b01-119">SMS alıcısının ülke kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7b01-119">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="d7b01-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b01-120">-DefaultProfile</span></span>
<span data-ttu-id="d7b01-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d7b01-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7b01-122">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="d7b01-122">-EmailAddress</span></span>
<span data-ttu-id="d7b01-123">E-posta alıcısının adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7b01-123">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="d7b01-124">-Emailahize</span><span class="sxs-lookup"><span data-stu-id="d7b01-124">-EmailReceiver</span></span>
<span data-ttu-id="d7b01-125">E-posta alıcısının oluşturulacağını belirtir</span><span class="sxs-lookup"><span data-stu-id="d7b01-125">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="d7b01-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="d7b01-126">-Name</span></span>
<span data-ttu-id="d7b01-127">Alıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7b01-127">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="d7b01-128">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="d7b01-128">-PhoneNumber</span></span>
<span data-ttu-id="d7b01-129">SMS alıcısının telefon numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7b01-129">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="d7b01-130">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="d7b01-130">-ServiceUri</span></span>
<span data-ttu-id="d7b01-131">Web kancası alıcısının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7b01-131">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="d7b01-132">-Smsahize</span><span class="sxs-lookup"><span data-stu-id="d7b01-132">-SmsReceiver</span></span>
<span data-ttu-id="d7b01-133">SMS alıcısı oluşturulacağını belirtir</span><span class="sxs-lookup"><span data-stu-id="d7b01-133">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="d7b01-134">-Webalıcıalıcı</span><span class="sxs-lookup"><span data-stu-id="d7b01-134">-WebhookReceiver</span></span>
<span data-ttu-id="d7b01-135">Web kancası alıcısının oluşturulacağını belirtir</span><span class="sxs-lookup"><span data-stu-id="d7b01-135">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="d7b01-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b01-136">CommonParameters</span></span>
<span data-ttu-id="d7b01-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7b01-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b01-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7b01-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b01-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7b01-139">INPUTS</span></span>

### <span data-ttu-id="d7b01-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d7b01-140">System.String</span></span>

### <span data-ttu-id="d7b01-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d7b01-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d7b01-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7b01-142">OUTPUTS</span></span>

### <span data-ttu-id="d7b01-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="d7b01-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="d7b01-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7b01-144">NOTES</span></span>

## <span data-ttu-id="d7b01-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7b01-145">RELATED LINKS</span></span>

<span data-ttu-id="d7b01-146">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="d7b01-146">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
