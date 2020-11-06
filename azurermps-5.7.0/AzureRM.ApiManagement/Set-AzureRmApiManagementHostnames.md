---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F9CE8705-F7B1-45AB-98BC-FC6DC023D38D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementhostnames
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
ms.openlocfilehash: d48d1913a30fc03ca0ebaf86195b981a6ebe70fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594509"
---
# <span data-ttu-id="cf624-101">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="cf624-101">Set-AzureRmApiManagementHostnames</span></span>

## <span data-ttu-id="cf624-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf624-102">SYNOPSIS</span></span>
<span data-ttu-id="cf624-103">API yönetim hizmeti proxy 'si veya portalı için özel bir ana bilgisayar yapılandırması ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cf624-103">Sets a custom hostname configuration for an API Management service proxy or portal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf624-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf624-104">SYNTAX</span></span>

### <span data-ttu-id="cf624-105">SetSpecificService (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cf624-105">SetSpecificService (Default)</span></span>
```
Set-AzureRmApiManagementHostnames -ResourceGroupName <String> -Name <String>
 [-PortalHostnameConfiguration <PsApiManagementHostnameConfiguration>]
 [-ProxyHostnameConfiguration <PsApiManagementHostnameConfiguration>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf624-106">Setfrompsapsananagementınstance</span><span class="sxs-lookup"><span data-stu-id="cf624-106">SetFromPsApiManagementInstance</span></span>
```
Set-AzureRmApiManagementHostnames -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf624-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf624-107">DESCRIPTION</span></span>
<span data-ttu-id="cf624-108">**Set-Azurermapımanagementhostnames** cmdlet 'ı bir API yönetim hizmeti proxy 'si veya portalı için özel bir ana bilgisayar yapılandırması uygular.</span><span class="sxs-lookup"><span data-stu-id="cf624-108">The **Set-AzureRmApiManagementHostnames** cmdlet applies a custom hostname configuration for an API Management service proxy or portal.</span></span>

## <span data-ttu-id="cf624-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf624-109">EXAMPLES</span></span>

### <span data-ttu-id="cf624-110">Örnek 1: proxy ve Portal için özel ana bilgisayar yapılandırmasını ayarlama</span><span class="sxs-lookup"><span data-stu-id="cf624-110">Example 1: Set the custom hostname configuration for a proxy and portal</span></span>
```
PS C:\>Set-AzureRmApiManagementHostnames -Name ContosoApi -ResourceGroupName Contoso -PortalHostnameConfiguration $portalHostnameConf -ProxyHostnameConfiguration $proxyHostnameConf
```

<span data-ttu-id="cf624-111">Bu komut proxy ve Portal için özel ana bilgisayar yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cf624-111">This command sets the custom hostname configuration for proxy and portal.</span></span>

### <span data-ttu-id="cf624-112">Örnek 2: proxy ve Portal için özel bir ana bilgisayar adı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="cf624-112">Example 2: Configure a custom hostname for a proxy and portal</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name ContosoApi -ResourceGroupName "Contoso" -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
PS C:\> Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName "Contoso" -HostnameType "Portal" -PfxPath "C:\portalcert.pfx" -PfxPassword "CertSecret"
PS C:\> $PortalHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
PS C:\> $ProxyHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "proxy.contoso.com" -CertificateThumbprint "5DD7CCF6A1E74E0987DD2873406B7264"
PS C:\> Set-AzureRmApiManagementHostnames -Name "ContosoApi" -ResourceGroupName "Contoso" -PortalHostnameConfiguration $PortalHostnameConf -ProxyHostnameConfiguration $ProxyHostnameConf
```

<span data-ttu-id="cf624-113">Bu örnekte, proxy ve Portal için özel bir ana bilgisayar adı yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="cf624-113">This example configures a custom hostname for proxy and portal.</span></span>
<span data-ttu-id="cf624-114">İlgili sertifikaları almanız ve özel ana bilgisayar adlarını uygulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="cf624-114">You need to import corresponding certificates and then apply the custom hostnames.</span></span>

## <span data-ttu-id="cf624-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf624-115">PARAMETERS</span></span>

### <span data-ttu-id="cf624-116">-Ucuz</span><span class="sxs-lookup"><span data-stu-id="cf624-116">-ApiManagement</span></span>
<span data-ttu-id="cf624-117">Bu cmdlet 'in *portalhostnameconfiguration* ve *proxyhostnameconfiguration* parametrelerini aldığı **psapimana,** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf624-117">Specifies the **PsApiManagement** instance that this cmdlet gets the *PortalHostnameConfiguration* and *ProxyHostnameConfiguration* parameters from.</span></span>

```yaml
Type: PsApiManagement
Parameter Sets: SetFromPsApiManagementInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf624-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf624-118">-DefaultProfile</span></span>
<span data-ttu-id="cf624-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cf624-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="cf624-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="cf624-120">-Name</span></span>
<span data-ttu-id="cf624-121">API yönetim örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf624-121">Specifies the name of the API Management instance.</span></span>

```yaml
Type: String
Parameter Sets: SetSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf624-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cf624-122">-PassThru</span></span>
<span data-ttu-id="cf624-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="cf624-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cf624-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="cf624-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf624-125">-PortalHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf624-125">-PortalHostnameConfiguration</span></span>
<span data-ttu-id="cf624-126">Özel Portal ana bilgisayar yapılandırması 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf624-126">Specifies the custom portal hostname configuration.</span></span>
<span data-ttu-id="cf624-127">Cmdlet 'e $null geçirilirken varsayılan ana bilgisayar adı ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="cf624-127">Passing $null to the cmdlet sets the default hostname.</span></span>

```yaml
Type: PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf624-128">-ProxyHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf624-128">-ProxyHostnameConfiguration</span></span>
<span data-ttu-id="cf624-129">Özel proxy ana bilgisayar yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf624-129">Specifies the custom proxy hostname configuration.</span></span>
<span data-ttu-id="cf624-130">$Null geçirilen varsayılan ana bilgisayar adı ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="cf624-130">Passing $null sets the default hostname.</span></span>

```yaml
Type: PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf624-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf624-131">-ResourceGroupName</span></span>
<span data-ttu-id="cf624-132">API yönetim örneğinin altında bulunduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf624-132">Specifies the name of the resource group under which the API Management instance exists.</span></span>

```yaml
Type: String
Parameter Sets: SetSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf624-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf624-133">CommonParameters</span></span>
<span data-ttu-id="cf624-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf624-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf624-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf624-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf624-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf624-136">INPUTS</span></span>

### <span data-ttu-id="cf624-137">Bağış</span><span class="sxs-lookup"><span data-stu-id="cf624-137">PsApiManagement</span></span>
<span data-ttu-id="cf624-138">Parametre ' Apsananadeğeri ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="cf624-138">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="cf624-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf624-139">OUTPUTS</span></span>

### <span data-ttu-id="cf624-140">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="cf624-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="cf624-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf624-141">NOTES</span></span>

## <span data-ttu-id="cf624-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf624-142">RELATED LINKS</span></span>

[<span data-ttu-id="cf624-143">Import-Azurermapımanagementhostnamecertificate</span><span class="sxs-lookup"><span data-stu-id="cf624-143">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="cf624-144">Yeni-Azurermapımanagementhostnameconfiguration</span><span class="sxs-lookup"><span data-stu-id="cf624-144">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)


