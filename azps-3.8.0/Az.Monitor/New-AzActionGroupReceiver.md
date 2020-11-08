---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: f2862c08212f5e41de10cb600edb22c38eac68d4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098464"
---
# <span data-ttu-id="e8b51-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="e8b51-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="e8b51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8b51-102">SYNOPSIS</span></span>
<span data-ttu-id="e8b51-103">Yeni bir eylem grubu alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e8b51-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="e8b51-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8b51-104">SYNTAX</span></span>

### <span data-ttu-id="e8b51-105">Newemailalıcı(varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e8b51-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8b51-106">Newsmsalıcısı</span><span class="sxs-lookup"><span data-stu-id="e8b51-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8b51-107">Newwebalıcıalıcı</span><span class="sxs-lookup"><span data-stu-id="e8b51-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8b51-108">Newalıalıcı</span><span class="sxs-lookup"><span data-stu-id="e8b51-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8b51-109">Newvoicerecever</span><span class="sxs-lookup"><span data-stu-id="e8b51-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8b51-110">Newarmrolerecever</span><span class="sxs-lookup"><span data-stu-id="e8b51-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8b51-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="e8b51-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8b51-112">Newlogicappahize</span><span class="sxs-lookup"><span data-stu-id="e8b51-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8b51-113">Newautomationrunbookalıcısı</span><span class="sxs-lookup"><span data-stu-id="e8b51-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8b51-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="e8b51-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8b51-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8b51-115">DESCRIPTION</span></span>
<span data-ttu-id="e8b51-116">**Yeni-Azactiongroupahize** cmdlet 'i bellekte yeni eylem grubu alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e8b51-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="e8b51-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8b51-117">EXAMPLES</span></span>

### <span data-ttu-id="e8b51-118">Örnek 1: bellekte yeni bir e-posta alıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e8b51-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="e8b51-119">Bu komut bellekte yeni bir e-posta alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e8b51-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="e8b51-120">Örnek 2: bellekte yeni bir SMS alıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e8b51-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="e8b51-121">Bu komut bellekte yeni bir SMS alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e8b51-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="e8b51-122">Örnek 3: bellekte yeni bir Web kancası alıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e8b51-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="e8b51-123">Bu komut bellekte yeni bir Web kancası alıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e8b51-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="e8b51-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8b51-124">PARAMETERS</span></span>

### <span data-ttu-id="e8b51-125">-Armrolerecever</span><span class="sxs-lookup"><span data-stu-id="e8b51-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="e8b51-126">Armrolerecever oluşturma</span><span class="sxs-lookup"><span data-stu-id="e8b51-126">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-127">-Automationaccountıd</span><span class="sxs-lookup"><span data-stu-id="e8b51-127">-AutomationAccountId</span></span>
<span data-ttu-id="e8b51-128">Automationaccountıd</span><span class="sxs-lookup"><span data-stu-id="e8b51-128">the AutomationAccountId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-129">-Automationrunbookalıcıdır</span><span class="sxs-lookup"><span data-stu-id="e8b51-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="e8b51-130">Automationrunbookalıcıoluşturma</span><span class="sxs-lookup"><span data-stu-id="e8b51-130">Create a AutomationRunbookReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="e8b51-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="e8b51-132">Web kancaları 'nın gönderilmesi gereken URI</span><span class="sxs-lookup"><span data-stu-id="e8b51-132">the URI where webhooks should be sent</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e8b51-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="e8b51-134">AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e8b51-134">the AzureAppPushEmailAddress</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="e8b51-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="e8b51-136">AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="e8b51-136">Create a AzureAppPushReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="e8b51-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="e8b51-138">Armrolerecever oluşturma</span><span class="sxs-lookup"><span data-stu-id="e8b51-138">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="e8b51-139">-CallbackUrl</span></span>
<span data-ttu-id="e8b51-140">Çağrı Backurl</span><span class="sxs-lookup"><span data-stu-id="e8b51-140">the CallbackUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-141">-ConnectionID</span><span class="sxs-lookup"><span data-stu-id="e8b51-141">-ConnectionId</span></span>
<span data-ttu-id="e8b51-142">Bu alıcının ISM bağlantı kimliği</span><span class="sxs-lookup"><span data-stu-id="e8b51-142">the itsm connection id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="e8b51-143">-CountryCode</span></span>
<span data-ttu-id="e8b51-144">SMS alıcısının ülke kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8b51-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="e8b51-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8b51-145">-DefaultProfile</span></span>
<span data-ttu-id="e8b51-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e8b51-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8b51-147">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="e8b51-147">-EmailAddress</span></span>
<span data-ttu-id="e8b51-148">E-posta alıcısının adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8b51-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="e8b51-149">-Emailahize</span><span class="sxs-lookup"><span data-stu-id="e8b51-149">-EmailReceiver</span></span>
<span data-ttu-id="e8b51-150">E-posta alıcısının oluşturulacağını belirtir</span><span class="sxs-lookup"><span data-stu-id="e8b51-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="e8b51-151">-Functionappresourceıd</span><span class="sxs-lookup"><span data-stu-id="e8b51-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="e8b51-152">işlev uygulaması RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e8b51-152">the function app resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-153">-Fonksiyonadı</span><span class="sxs-lookup"><span data-stu-id="e8b51-153">-FunctionName</span></span>
<span data-ttu-id="e8b51-154">Fonksiyonadı</span><span class="sxs-lookup"><span data-stu-id="e8b51-154">the functionName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-155">-HttpTriggerUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="e8b51-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="e8b51-156">httpTriggerUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="e8b51-156">the httpTriggerUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-157">-Identifieruri</span><span class="sxs-lookup"><span data-stu-id="e8b51-157">-IdentifierUri</span></span>
<span data-ttu-id="e8b51-158">aad kimlik doğrulaması için tanımlayıcı URI 'si</span><span class="sxs-lookup"><span data-stu-id="e8b51-158">the Identifier uri for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-159">-Isglobalrunbook</span><span class="sxs-lookup"><span data-stu-id="e8b51-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="e8b51-160">Bu örneğin genel runbook olup olmadığını gösteren</span><span class="sxs-lookup"><span data-stu-id="e8b51-160">indicating whether this instance is global runbook</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-161">-Itsmahize</span><span class="sxs-lookup"><span data-stu-id="e8b51-161">-ItsmReceiver</span></span>
<span data-ttu-id="e8b51-162">Itsmahize oluşturma</span><span class="sxs-lookup"><span data-stu-id="e8b51-162">Create a ItsmReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewItsmReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-163">-Logicappahize</span><span class="sxs-lookup"><span data-stu-id="e8b51-163">-LogicAppReceiver</span></span>
<span data-ttu-id="e8b51-164">Logicappahize oluşturma</span><span class="sxs-lookup"><span data-stu-id="e8b51-164">Create a LogicAppReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-165">-Ad</span><span class="sxs-lookup"><span data-stu-id="e8b51-165">-Name</span></span>
<span data-ttu-id="e8b51-166">Alıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8b51-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="e8b51-167">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="e8b51-167">-ObjectId</span></span>
<span data-ttu-id="e8b51-168">aad kimlik doğrulaması için Web kancası uygulama nesnesi kimliği</span><span class="sxs-lookup"><span data-stu-id="e8b51-168">the webhook app object Id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-169">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="e8b51-169">-PhoneNumber</span></span>
<span data-ttu-id="e8b51-170">SMS alıcısının telefon numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8b51-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="e8b51-171">-Bölge</span><span class="sxs-lookup"><span data-stu-id="e8b51-171">-Region</span></span>
<span data-ttu-id="e8b51-172">Bu alıcının ISM bölgesi</span><span class="sxs-lookup"><span data-stu-id="e8b51-172">the itsm Region of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-173">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e8b51-173">-ResourceId</span></span>
<span data-ttu-id="e8b51-174">RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e8b51-174">the ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-175">-RoleID</span><span class="sxs-lookup"><span data-stu-id="e8b51-175">-RoleId</span></span>
<span data-ttu-id="e8b51-176">Alıcının ARM rol kimliği</span><span class="sxs-lookup"><span data-stu-id="e8b51-176">The arm role id of the receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="e8b51-177">-RunbookName</span></span>
<span data-ttu-id="e8b51-178">RunbookName</span><span class="sxs-lookup"><span data-stu-id="e8b51-178">the RunbookName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="e8b51-179">-ServiceUri</span></span>
<span data-ttu-id="e8b51-180">Web kancası alıcısının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8b51-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="e8b51-181">-Smsahize</span><span class="sxs-lookup"><span data-stu-id="e8b51-181">-SmsReceiver</span></span>
<span data-ttu-id="e8b51-182">SMS alıcısı oluşturulacağını belirtir</span><span class="sxs-lookup"><span data-stu-id="e8b51-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="e8b51-183">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="e8b51-183">-TenantId</span></span>
<span data-ttu-id="e8b51-184">aad kimlik doğrulaması için Kiracı kimliği</span><span class="sxs-lookup"><span data-stu-id="e8b51-184">the tenant id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-185">-Bilet yapılandırması</span><span class="sxs-lookup"><span data-stu-id="e8b51-185">-TicketConfiguration</span></span>
<span data-ttu-id="e8b51-186">Bu alıcının ITSM anahtar yapılandırması</span><span class="sxs-lookup"><span data-stu-id="e8b51-186">the itsm TicketConfiguration of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="e8b51-187">-UseAadAuth</span></span>
<span data-ttu-id="e8b51-188">Add auth Use bayrağı</span><span class="sxs-lookup"><span data-stu-id="e8b51-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="e8b51-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="e8b51-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="e8b51-190">Genel uyarı şemasının kullanılıp kullanılmayacağını bayrak.</span><span class="sxs-lookup"><span data-stu-id="e8b51-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="e8b51-191">Bu değer SMS, Azure Uygulama itme, ıTSM ve sesli recıevers için neglezererecektir.</span><span class="sxs-lookup"><span data-stu-id="e8b51-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="e8b51-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="e8b51-192">-VoiceCountryCode</span></span>
<span data-ttu-id="e8b51-193">Ses alıcısının ülke kodu</span><span class="sxs-lookup"><span data-stu-id="e8b51-193">The country code of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-194">-Sesli telefon numarası</span><span class="sxs-lookup"><span data-stu-id="e8b51-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="e8b51-195">Ses alıcısının telefon numarası</span><span class="sxs-lookup"><span data-stu-id="e8b51-195">The phone number of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-196">-Voicerecever</span><span class="sxs-lookup"><span data-stu-id="e8b51-196">-VoiceReceiver</span></span>
<span data-ttu-id="e8b51-197">Sesli alıcı oluşturma</span><span class="sxs-lookup"><span data-stu-id="e8b51-197">Create a voice receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-198">-Webalıcıalıcı</span><span class="sxs-lookup"><span data-stu-id="e8b51-198">-WebhookReceiver</span></span>
<span data-ttu-id="e8b51-199">Web kancası alıcısının oluşturulacağını belirtir</span><span class="sxs-lookup"><span data-stu-id="e8b51-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="e8b51-200">-Webkancası RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e8b51-200">-WebhookResourceId</span></span>
<span data-ttu-id="e8b51-201">Web, RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e8b51-201">the WebhookResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-202">-</span><span class="sxs-lookup"><span data-stu-id="e8b51-202">-WorkspaceId</span></span>
<span data-ttu-id="e8b51-203">Bu alıcının itsm çalışma alanı kimliği</span><span class="sxs-lookup"><span data-stu-id="e8b51-203">the itsm workspace id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b51-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8b51-204">CommonParameters</span></span>
<span data-ttu-id="e8b51-205">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8b51-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8b51-206">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e8b51-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8b51-207">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8b51-207">INPUTS</span></span>

### <span data-ttu-id="e8b51-208">System. String</span><span class="sxs-lookup"><span data-stu-id="e8b51-208">System.String</span></span>

### <span data-ttu-id="e8b51-209">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e8b51-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e8b51-210">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8b51-210">OUTPUTS</span></span>

### <span data-ttu-id="e8b51-211">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="e8b51-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="e8b51-212">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8b51-212">NOTES</span></span>

## <span data-ttu-id="e8b51-213">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8b51-213">RELATED LINKS</span></span>

<span data-ttu-id="e8b51-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="e8b51-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
