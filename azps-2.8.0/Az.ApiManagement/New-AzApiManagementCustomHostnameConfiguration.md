---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: 534ea482f2d2e1ae172c1eba0c953272750a228f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753526"
---
# <span data-ttu-id="d8089-101">New-AzApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8089-101">New-AzApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="d8089-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8089-102">SYNOPSIS</span></span>
<span data-ttu-id="d8089-103">Örneği oluşturur `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="d8089-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

## <span data-ttu-id="d8089-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8089-104">SYNTAX</span></span>

### <span data-ttu-id="d8089-105">Nochangecercertificate (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d8089-105">NoChangeCertificate (Default)</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8089-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="d8089-106">SslCertificateFromFile</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -PfxPath <String> [-PfxPassword <SecureString>] [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8089-107">Sslcertificatefromkeykasası</span><span class="sxs-lookup"><span data-stu-id="d8089-107">SslCertificateFromKeyVault</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -KeyVaultId <String> [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8089-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8089-108">DESCRIPTION</span></span>
<span data-ttu-id="d8089-109">**Yeni-Azapsananagementcustomhostnameconfiguration** cmdlet 'ı, **Psapimanagementcustomhostnameconfiguration** örneğini oluşturan bir yardımcı komuttur.</span><span class="sxs-lookup"><span data-stu-id="d8089-109">The **New-AzApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="d8089-110">Bu komut New-AzApiManagement ve Set-AzApiManagement cmdlet 'inde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d8089-110">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="d8089-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8089-111">EXAMPLES</span></span>

### <span data-ttu-id="d8089-112">Örnek 1: dosyadan SSL sertifikası kullanarak PsApiManagementCustomHostNameConfiguration örneğini oluşturma ve başlatma</span><span class="sxs-lookup"><span data-stu-id="d8089-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="d8089-113">Bu komut, Portal için **Psapimanagementcustomhostnameconfiguration** örneğini oluşturur ve başlatır.</span><span class="sxs-lookup"><span data-stu-id="d8089-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="d8089-114">Ardından özel ana bilgisayar yapılandırması ile yeni bir anlık hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8089-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="d8089-115">Örnek 2: Keykasa kaynağından parola kullanarak PsApiManagementCustomHostNameConfiguration örneğini oluşturma ve başlatma</span><span class="sxs-lookup"><span data-stu-id="d8089-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -AssignIdentity
```

<span data-ttu-id="d8089-116">Bu komut **Psapimanagementcustomhostnameconfiguration** örneğini oluşturur ve başlatır.</span><span class="sxs-lookup"><span data-stu-id="d8089-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="d8089-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8089-117">PARAMETERS</span></span>

### <span data-ttu-id="d8089-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8089-118">-DefaultProfile</span></span>
<span data-ttu-id="d8089-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8089-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8089-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="d8089-120">-DefaultSslBinding</span></span>
<span data-ttu-id="d8089-121">Değerin gizli olup olmadığını ve şifrelenmesi gerektiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="d8089-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="d8089-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d8089-122">This parameter is optional.</span></span>
<span data-ttu-id="d8089-123">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="d8089-123">Default Value is false.</span></span>

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

### <span data-ttu-id="d8089-124">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="d8089-124">-Hostname</span></span>
<span data-ttu-id="d8089-125">Özel ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="d8089-125">Custom Hostname</span></span>

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

### <span data-ttu-id="d8089-126">-Hostnamecertificateınformation</span><span class="sxs-lookup"><span data-stu-id="d8089-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="d8089-127">Var olan sertifika yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="d8089-127">Existing Certificate Configuration.</span></span>

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

### <span data-ttu-id="d8089-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="d8089-128">-HostnameType</span></span>
<span data-ttu-id="d8089-129">Ana bilgisayar türü</span><span class="sxs-lookup"><span data-stu-id="d8089-129">Hostname Type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm, DeveloperPortal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8089-130">-Anahtarlı</span><span class="sxs-lookup"><span data-stu-id="d8089-130">-KeyVaultId</span></span>
<span data-ttu-id="d8089-131">Anahtar özel SSL sertifikasını depolayan gizli kod dizesi.</span><span class="sxs-lookup"><span data-stu-id="d8089-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

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

### <span data-ttu-id="d8089-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d8089-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="d8089-133">Değerin gizli olup olmadığını ve şifrelenmesi gerektiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="d8089-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="d8089-134">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d8089-134">This parameter is optional.</span></span>
<span data-ttu-id="d8089-135">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="d8089-135">Default Value is false.</span></span>

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

### <span data-ttu-id="d8089-136">-Pfxparolası</span><span class="sxs-lookup"><span data-stu-id="d8089-136">-PfxPassword</span></span>
<span data-ttu-id="d8089-137">. Pfx sertifika dosyasının parolası.</span><span class="sxs-lookup"><span data-stu-id="d8089-137">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="d8089-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="d8089-138">-PfxPath</span></span>
<span data-ttu-id="d8089-139">. Pfx sertifika dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="d8089-139">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="d8089-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8089-140">CommonParameters</span></span>
<span data-ttu-id="d8089-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8089-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8089-142">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d8089-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8089-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8089-143">INPUTS</span></span>

### <span data-ttu-id="d8089-144">Microsoft. Azure. Commands. apsananad</span><span class="sxs-lookup"><span data-stu-id="d8089-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="d8089-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8089-145">OUTPUTS</span></span>

### <span data-ttu-id="d8089-146">Microsoft. Azure. Commands. Apsananad. modeller. Psapsananagementcustomhostnameconfiguration</span><span class="sxs-lookup"><span data-stu-id="d8089-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="d8089-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8089-147">NOTES</span></span>

## <span data-ttu-id="d8089-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8089-148">RELATED LINKS</span></span>

[<span data-ttu-id="d8089-149">Yeni-azlı bir</span><span class="sxs-lookup"><span data-stu-id="d8089-149">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="d8089-150">Set-azapsanana</span><span class="sxs-lookup"><span data-stu-id="d8089-150">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)