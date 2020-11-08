---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 9505194ef562c7faf292d5bbf2fe3de20ac7995f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104799"
---
# <span data-ttu-id="1b6e9-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1b6e9-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1b6e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b6e9-102">SYNOPSIS</span></span>
<span data-ttu-id="1b6e9-103">Uygulama ağ geçidi için HTTP dinleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="1b6e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b6e9-104">SYNTAX</span></span>

### <span data-ttu-id="1b6e9-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="1b6e9-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-HostName <String>]
 [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b6e9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1b6e9-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b6e9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b6e9-107">DESCRIPTION</span></span>
<span data-ttu-id="1b6e9-108">**Yeni-AzApplicationGatewayHttpListener** cmdlet 'ı bir Azure uygulama ağ GEÇIDI için http dinleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="1b6e9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b6e9-109">EXAMPLES</span></span>

### <span data-ttu-id="1b6e9-110">Örnek 1: HTTP dinleyicisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1b6e9-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="1b6e9-111">Bu komut Listener01 adlı bir HTTP dinleyicisi oluşturur ve sonucu $Listener adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="1b6e9-112">Örnek 2: SSL ile HTTP dinleyicisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1b6e9-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="1b6e9-113">Bu komut SSL boşaltması kullanan bir HTTP dinleyicisi oluşturur ve $SSLCert 01 değişkeninde SSL sertifikası sağlar.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="1b6e9-114">Komut sonucu $Listener adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="1b6e9-115">Örnek 3: güvenlik duvarıyla HTTP dinleyicisi oluşturma-ilke</span><span class="sxs-lookup"><span data-stu-id="1b6e9-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="1b6e9-116">Bu komut Listener01, Firewall$firewallPolicy Policy adlı bir HTTP dinleyicisi oluşturur ve sonucu $Listener adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="1b6e9-117">Örnek 4: SSL ve ana bilgisayar adları içeren HTTPS dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="1b6e9-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="1b6e9-118">Bu komut, SSL boşaltması kullanan bir HTTP dinleyicisi oluşturur ve $SSLCert 01 değişkeninde iki konak adıyla birlikte SSL sertifikası sağlar.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="1b6e9-119">Komut sonucu $Listener adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="1b6e9-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b6e9-120">PARAMETERS</span></span>

### <span data-ttu-id="1b6e9-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b6e9-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="1b6e9-122">Uygulama ağ geçidinde müşteri hatası</span><span class="sxs-lookup"><span data-stu-id="1b6e9-122">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6e9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b6e9-123">-DefaultProfile</span></span>
<span data-ttu-id="1b6e9-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b6e9-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1b6e9-125">-FirewallPolicy</span></span>
<span data-ttu-id="1b6e9-126">Üst düzey güvenlik duvarı ilkesine nesne başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="1b6e9-127">Nesne başvurusu, New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="1b6e9-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-Name "wafPolicy1"-ResourceGroup "rgName" yukarıdaki commandizin kullanılarak oluşturulan bir güvenlik duvarı ilkesine yol kuralı düzeyinde başvurulabilir.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="1b6e9-129">Yukarıdaki komut komutu varsayılan ilke ayarları ve yönetilen kurallar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="1b6e9-130">Varsayılan değerler yerine, kullanıcılar sırasıyla New-AzApplicationGatewayFirewallPolicySettings ve New-AzApplicationGatewayFirewallPolicyManagedRules kullanarak PolicySettings, ManagedRules değerlerini belirtebilir.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6e9-131">-Firewallpolicyıd</span><span class="sxs-lookup"><span data-stu-id="1b6e9-131">-FirewallPolicyId</span></span>
<span data-ttu-id="1b6e9-132">Var olan bir üst düzey Web uygulaması güvenlik duvarı kaynağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="1b6e9-133">Güvenlik Duvarı ilke kimlikleri, Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet kullanılarak döndürülebilir.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="1b6e9-134">KIMLIĞI doğruladıktan sonra *firewallpolicy* parametre yerine *Firewallpolicyıd* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="1b6e9-135">Örneğin:-Firewallpolicyıd/Subscriptions/<abonelik-No>/resourceGroups/<Resource-Group-ID>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="1b6e9-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6e9-136">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="1b6e9-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="1b6e9-137">HTTP dinleyicisi için ön uç IP yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6e9-138">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="1b6e9-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="1b6e9-139">HTTP dinleyicisi için ön uç IP yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6e9-140">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="1b6e9-140">-FrontendPort</span></span>
<span data-ttu-id="1b6e9-141">HTTP dinleyicisi için ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-141">Specifies the front-end port for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6e9-142">-Frontenvseçportıd</span><span class="sxs-lookup"><span data-stu-id="1b6e9-142">-FrontendPortId</span></span>
<span data-ttu-id="1b6e9-143">HTTP dinleyicisi için ön uç bağlantı noktası nesnesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6e9-144">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="1b6e9-144">-HostName</span></span>
<span data-ttu-id="1b6e9-145">Uygulama ağ geçidi HTTP dinleyicisinin ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-145">Specifies the host name of the application gateway HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6e9-146">-Ana makine adları</span><span class="sxs-lookup"><span data-stu-id="1b6e9-146">-HostNames</span></span>
<span data-ttu-id="1b6e9-147">Ana bilgisayar adları</span><span class="sxs-lookup"><span data-stu-id="1b6e9-147">Host names</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6e9-148">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b6e9-148">-Name</span></span>
<span data-ttu-id="1b6e9-149">Bu cmdlet 'in oluşturduğu HTTP dinleyicisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6e9-150">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="1b6e9-150">-Protocol</span></span>
<span data-ttu-id="1b6e9-151">HTTP dinleyicisinin kullandığı protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-151">Specifies the protocol that the HTTP listener uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6e9-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="1b6e9-152">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6e9-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="1b6e9-153">-SslCertificate</span></span>
<span data-ttu-id="1b6e9-154">HTTP dinleyicisi için SSL sertifikası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6e9-155">-Sslcertificateıd</span><span class="sxs-lookup"><span data-stu-id="1b6e9-155">-SslCertificateId</span></span>
<span data-ttu-id="1b6e9-156">HTTP dinleyicisi için SSL sertifikasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6e9-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b6e9-157">CommonParameters</span></span>
<span data-ttu-id="1b6e9-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b6e9-159">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b6e9-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b6e9-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b6e9-160">INPUTS</span></span>

### <span data-ttu-id="1b6e9-161">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1b6e9-161">None</span></span>

## <span data-ttu-id="1b6e9-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b6e9-162">OUTPUTS</span></span>

### <span data-ttu-id="1b6e9-163">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1b6e9-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1b6e9-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b6e9-164">NOTES</span></span>

## <span data-ttu-id="1b6e9-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b6e9-165">RELATED LINKS</span></span>

[<span data-ttu-id="1b6e9-166">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1b6e9-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1b6e9-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1b6e9-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1b6e9-168">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1b6e9-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1b6e9-169">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1b6e9-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


