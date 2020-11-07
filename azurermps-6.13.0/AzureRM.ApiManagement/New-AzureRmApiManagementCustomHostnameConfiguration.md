---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: 2f929fc2968935284024e1112e62b395aa0d545e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763515"
---
# <span data-ttu-id="a03bb-101">New-AzureRmApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a03bb-101">New-AzureRmApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="a03bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a03bb-102">SYNOPSIS</span></span>
<span data-ttu-id="a03bb-103">Örneği oluşturur `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="a03bb-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a03bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a03bb-104">SYNTAX</span></span>

### <span data-ttu-id="a03bb-105">Nochangecercertificate (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a03bb-105">NoChangeCertificate (Default)</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a03bb-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="a03bb-106">SslCertificateFromFile</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultSslBinding] [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a03bb-107">Sslcertificatefromkeykasası</span><span class="sxs-lookup"><span data-stu-id="a03bb-107">SslCertificateFromKeyVault</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType> -KeyVaultId <String> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a03bb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a03bb-108">DESCRIPTION</span></span>
<span data-ttu-id="a03bb-109">**New-Azurermapsananagementcustomhostnameconfiguration** cmdlet 'ı, **Psapimanagementcustomhostnameconfiguration** örneğini oluşturan bir yardımcı komuttur.</span><span class="sxs-lookup"><span data-stu-id="a03bb-109">The **New-AzureRmApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="a03bb-110">Bu komut New-AzureRmApiManagement ve Set-AzureRmApiManagement cmdlet 'inde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a03bb-110">This command is used with the New-AzureRmApiManagement and Set-AzureRmApiManagement cmdlet.</span></span>

## <span data-ttu-id="a03bb-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a03bb-111">EXAMPLES</span></span>

### <span data-ttu-id="a03bb-112">Örnek 1: dosyadan SSL sertifikası kullanarak PsApiManagementCustomHostNameConfiguration örneğini oluşturma ve başlatma</span><span class="sxs-lookup"><span data-stu-id="a03bb-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="a03bb-113">Bu komut, Portal için **Psapimanagementcustomhostnameconfiguration** örneğini oluşturur ve başlatır.</span><span class="sxs-lookup"><span data-stu-id="a03bb-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="a03bb-114">Ardından özel ana bilgisayar yapılandırması ile yeni bir anlık hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a03bb-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="a03bb-115">Örnek 2: Keykasa kaynağından parola kullanarak PsApiManagementCustomHostNameConfiguration örneğini oluşturma ve başlatma</span><span class="sxs-lookup"><span data-stu-id="a03bb-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -AssignIdentity
```

<span data-ttu-id="a03bb-116">Bu komut **Psapimanagementcustomhostnameconfiguration** örneğini oluşturur ve başlatır.</span><span class="sxs-lookup"><span data-stu-id="a03bb-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="a03bb-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a03bb-117">PARAMETERS</span></span>

### <span data-ttu-id="a03bb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a03bb-118">-DefaultProfile</span></span>
<span data-ttu-id="a03bb-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a03bb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a03bb-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="a03bb-120">-DefaultSslBinding</span></span>
<span data-ttu-id="a03bb-121">Değerin gizli olup olmadığını ve şifrelenmesi gerektiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="a03bb-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="a03bb-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a03bb-122">This parameter is optional.</span></span>
<span data-ttu-id="a03bb-123">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="a03bb-123">Default Value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03bb-124">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="a03bb-124">-Hostname</span></span>
<span data-ttu-id="a03bb-125">Özel ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="a03bb-125">Custom Hostname</span></span>

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

### <span data-ttu-id="a03bb-126">-Hostnamecertificateınformation</span><span class="sxs-lookup"><span data-stu-id="a03bb-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="a03bb-127">Var olan sertifika yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="a03bb-127">Existing Certificate Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation
Parameter Sets: NoChangeCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a03bb-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="a03bb-128">-HostnameType</span></span>
<span data-ttu-id="a03bb-129">Ana bilgisayar türü</span><span class="sxs-lookup"><span data-stu-id="a03bb-129">Hostname Type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03bb-130">-Anahtarlı</span><span class="sxs-lookup"><span data-stu-id="a03bb-130">-KeyVaultId</span></span>
<span data-ttu-id="a03bb-131">Anahtar özel SSL sertifikasını depolayan gizli kod dizesi.</span><span class="sxs-lookup"><span data-stu-id="a03bb-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03bb-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a03bb-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="a03bb-133">Değerin gizli olup olmadığını ve şifrelenmesi gerektiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="a03bb-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="a03bb-134">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a03bb-134">This parameter is optional.</span></span>
<span data-ttu-id="a03bb-135">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="a03bb-135">Default Value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03bb-136">-Pfxparolası</span><span class="sxs-lookup"><span data-stu-id="a03bb-136">-PfxPassword</span></span>
<span data-ttu-id="a03bb-137">. Pfx sertifika dosyasının parolası.</span><span class="sxs-lookup"><span data-stu-id="a03bb-137">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SslCertificateFromFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03bb-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="a03bb-138">-PfxPath</span></span>
<span data-ttu-id="a03bb-139">. Pfx sertifika dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="a03bb-139">Path to a .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03bb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a03bb-140">CommonParameters</span></span>
<span data-ttu-id="a03bb-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a03bb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a03bb-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a03bb-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a03bb-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a03bb-143">INPUTS</span></span>

### <span data-ttu-id="a03bb-144">Microsoft. Azure. Commands. apsananad</span><span class="sxs-lookup"><span data-stu-id="a03bb-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="a03bb-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a03bb-145">OUTPUTS</span></span>

### <span data-ttu-id="a03bb-146">Microsoft. Azure. Commands. Apsananad. modeller. Psapsananagementcustomhostnameconfiguration</span><span class="sxs-lookup"><span data-stu-id="a03bb-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="a03bb-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a03bb-147">NOTES</span></span>

## <span data-ttu-id="a03bb-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a03bb-148">RELATED LINKS</span></span>

[<span data-ttu-id="a03bb-149">Yeni-azurermapı</span><span class="sxs-lookup"><span data-stu-id="a03bb-149">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="a03bb-150">Set-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="a03bb-150">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)
