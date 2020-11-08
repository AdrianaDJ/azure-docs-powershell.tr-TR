---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 9505194ef562c7faf292d5bbf2fe3de20ac7995f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267071"
---
# <span data-ttu-id="c8357-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c8357-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="c8357-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8357-102">SYNOPSIS</span></span>
<span data-ttu-id="c8357-103">Uygulama ağ geçidi için HTTP dinleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c8357-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="c8357-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8357-104">SYNTAX</span></span>

### <span data-ttu-id="c8357-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="c8357-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-HostName <String>]
 [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8357-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c8357-106">SetByResource</span></span>
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

## <span data-ttu-id="c8357-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8357-107">DESCRIPTION</span></span>
<span data-ttu-id="c8357-108">**Yeni-AzApplicationGatewayHttpListener** cmdlet 'ı bir Azure uygulama ağ GEÇIDI için http dinleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c8357-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="c8357-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8357-109">EXAMPLES</span></span>

### <span data-ttu-id="c8357-110">Örnek 1: HTTP dinleyicisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c8357-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="c8357-111">Bu komut Listener01 adlı bir HTTP dinleyicisi oluşturur ve sonucu $Listener adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="c8357-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="c8357-112">Örnek 2: SSL ile HTTP dinleyicisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c8357-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="c8357-113">Bu komut SSL boşaltması kullanan bir HTTP dinleyicisi oluşturur ve $SSLCert 01 değişkeninde SSL sertifikası sağlar.</span><span class="sxs-lookup"><span data-stu-id="c8357-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="c8357-114">Komut sonucu $Listener adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="c8357-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="c8357-115">Örnek 3: güvenlik duvarıyla HTTP dinleyicisi oluşturma-ilke</span><span class="sxs-lookup"><span data-stu-id="c8357-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="c8357-116">Bu komut Listener01, Firewall$firewallPolicy Policy adlı bir HTTP dinleyicisi oluşturur ve sonucu $Listener adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="c8357-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="c8357-117">Örnek 4: SSL ve ana bilgisayar adları içeren HTTPS dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="c8357-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="c8357-118">Bu komut, SSL boşaltması kullanan bir HTTP dinleyicisi oluşturur ve $SSLCert 01 değişkeninde iki konak adıyla birlikte SSL sertifikası sağlar.</span><span class="sxs-lookup"><span data-stu-id="c8357-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="c8357-119">Komut sonucu $Listener adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="c8357-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="c8357-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8357-120">PARAMETERS</span></span>

### <span data-ttu-id="c8357-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8357-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="c8357-122">Uygulama ağ geçidinde müşteri hatası</span><span class="sxs-lookup"><span data-stu-id="c8357-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="c8357-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8357-123">-DefaultProfile</span></span>
<span data-ttu-id="c8357-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c8357-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8357-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c8357-125">-FirewallPolicy</span></span>
<span data-ttu-id="c8357-126">Üst düzey güvenlik duvarı ilkesine nesne başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8357-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="c8357-127">Nesne başvurusu, New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="c8357-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="c8357-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-Name "wafPolicy1"-ResourceGroup "rgName" yukarıdaki commandizin kullanılarak oluşturulan bir güvenlik duvarı ilkesine yol kuralı düzeyinde başvurulabilir.</span><span class="sxs-lookup"><span data-stu-id="c8357-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="c8357-129">Yukarıdaki komut komutu varsayılan ilke ayarları ve yönetilen kurallar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c8357-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="c8357-130">Varsayılan değerler yerine, kullanıcılar sırasıyla New-AzApplicationGatewayFirewallPolicySettings ve New-AzApplicationGatewayFirewallPolicyManagedRules kullanarak PolicySettings, ManagedRules değerlerini belirtebilir.</span><span class="sxs-lookup"><span data-stu-id="c8357-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

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

### <span data-ttu-id="c8357-131">-Firewallpolicyıd</span><span class="sxs-lookup"><span data-stu-id="c8357-131">-FirewallPolicyId</span></span>
<span data-ttu-id="c8357-132">Var olan bir üst düzey Web uygulaması güvenlik duvarı kaynağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8357-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="c8357-133">Güvenlik Duvarı ilke kimlikleri, Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet kullanılarak döndürülebilir.</span><span class="sxs-lookup"><span data-stu-id="c8357-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="c8357-134">KIMLIĞI doğruladıktan sonra *firewallpolicy* parametre yerine *Firewallpolicyıd* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8357-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="c8357-135">Örneğin:-Firewallpolicyıd/Subscriptions/<abonelik-No>/resourceGroups/<Resource-Group-ID>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="c8357-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

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

### <span data-ttu-id="c8357-136">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="c8357-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="c8357-137">HTTP dinleyicisi için ön uç IP yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8357-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="c8357-138">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="c8357-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="c8357-139">HTTP dinleyicisi için ön uç IP yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8357-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="c8357-140">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="c8357-140">-FrontendPort</span></span>
<span data-ttu-id="c8357-141">HTTP dinleyicisi için ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8357-141">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="c8357-142">-Frontenvseçportıd</span><span class="sxs-lookup"><span data-stu-id="c8357-142">-FrontendPortId</span></span>
<span data-ttu-id="c8357-143">HTTP dinleyicisi için ön uç bağlantı noktası nesnesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8357-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="c8357-144">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="c8357-144">-HostName</span></span>
<span data-ttu-id="c8357-145">Uygulama ağ geçidi HTTP dinleyicisinin ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8357-145">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="c8357-146">-Ana makine adları</span><span class="sxs-lookup"><span data-stu-id="c8357-146">-HostNames</span></span>
<span data-ttu-id="c8357-147">Ana bilgisayar adları</span><span class="sxs-lookup"><span data-stu-id="c8357-147">Host names</span></span>

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

### <span data-ttu-id="c8357-148">-Ad</span><span class="sxs-lookup"><span data-stu-id="c8357-148">-Name</span></span>
<span data-ttu-id="c8357-149">Bu cmdlet 'in oluşturduğu HTTP dinleyicisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8357-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c8357-150">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="c8357-150">-Protocol</span></span>
<span data-ttu-id="c8357-151">HTTP dinleyicisinin kullandığı protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8357-151">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="c8357-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="c8357-152">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="c8357-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="c8357-153">-SslCertificate</span></span>
<span data-ttu-id="c8357-154">HTTP dinleyicisi için SSL sertifikası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8357-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="c8357-155">-Sslcertificateıd</span><span class="sxs-lookup"><span data-stu-id="c8357-155">-SslCertificateId</span></span>
<span data-ttu-id="c8357-156">HTTP dinleyicisi için SSL sertifikasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8357-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="c8357-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8357-157">CommonParameters</span></span>
<span data-ttu-id="c8357-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8357-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8357-159">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8357-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8357-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8357-160">INPUTS</span></span>

### <span data-ttu-id="c8357-161">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c8357-161">None</span></span>

## <span data-ttu-id="c8357-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8357-162">OUTPUTS</span></span>

### <span data-ttu-id="c8357-163">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c8357-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="c8357-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8357-164">NOTES</span></span>

## <span data-ttu-id="c8357-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8357-165">RELATED LINKS</span></span>

[<span data-ttu-id="c8357-166">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c8357-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="c8357-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c8357-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="c8357-168">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c8357-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="c8357-169">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c8357-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


