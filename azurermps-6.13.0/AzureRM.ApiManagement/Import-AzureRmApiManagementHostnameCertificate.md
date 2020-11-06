---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 98367100-4FFD-46F6-8974-603B32533626
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementhostnamecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
ms.openlocfilehash: 80bc75e8029db9aa4cac9f1e0abd53ad17c9fad1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589616"
---
# <span data-ttu-id="e45c8-101">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="e45c8-101">Import-AzureRmApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="e45c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e45c8-102">SYNOPSIS</span></span>
<span data-ttu-id="e45c8-103">Bir API yönetim hizmeti için PFX biçiminde bir sertifika içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="e45c8-103">Imports a certificate in a PFX format for an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e45c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e45c8-104">SYNTAX</span></span>

```
Import-AzureRmApiManagementHostnameCertificate -ResourceGroupName <String> -Name <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> -PfxPassword <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e45c8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e45c8-105">DESCRIPTION</span></span>
<span data-ttu-id="e45c8-106">**Import-Azurermapımanagementhostnamecertificate** cmdlet 'i, bir API yönetim HIZMETI için PFX biçiminde bir sertifika içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="e45c8-106">The **Import-AzureRmApiManagementHostnameCertificate** cmdlet imports a certificate in a PFX format for an API Management Service.</span></span>
<span data-ttu-id="e45c8-107">Sertifika özel konak adları yapılandırması için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e45c8-107">The certificate is to be used for custom hostnames configuration.</span></span>

## <span data-ttu-id="e45c8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e45c8-108">EXAMPLES</span></span>

### <span data-ttu-id="e45c8-109">Örnek 1: API Yönetimi ana bilgisayar sertifikasını Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="e45c8-109">Example 1: Import a API Management hostname certificate</span></span>
```powershell
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName Contoso -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
```

<span data-ttu-id="e45c8-110">Bu komut, bir proxy özel ana bilgisayar adı için sertifika alır.</span><span class="sxs-lookup"><span data-stu-id="e45c8-110">This command imports a certificate for a proxy custom hostname.</span></span>

## <span data-ttu-id="e45c8-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e45c8-111">PARAMETERS</span></span>

### <span data-ttu-id="e45c8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e45c8-112">-DefaultProfile</span></span>
<span data-ttu-id="e45c8-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e45c8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e45c8-114">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="e45c8-114">-HostnameType</span></span>
<span data-ttu-id="e45c8-115">Bu cmdlet 'in sertifikayı yüklediği ana bilgisayar adı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e45c8-115">Specifies the host name type that this cmdlet loads the certificate for.</span></span>
<span data-ttu-id="e45c8-116">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="e45c8-116">Valid values are:</span></span> 
- <span data-ttu-id="e45c8-117">Yi</span><span class="sxs-lookup"><span data-stu-id="e45c8-117">Proxy</span></span>
- <span data-ttu-id="e45c8-118">Portalınıza</span><span class="sxs-lookup"><span data-stu-id="e45c8-118">Portal</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e45c8-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="e45c8-119">-Name</span></span>
<span data-ttu-id="e45c8-120">Bu cmdlet 'in içeri aktardığından API yönetim dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e45c8-120">Specifies the name of the API Management deployment that this cmdlet imports.</span></span>

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

### <span data-ttu-id="e45c8-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e45c8-121">-PassThru</span></span>
<span data-ttu-id="e45c8-122">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="e45c8-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e45c8-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="e45c8-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e45c8-124">-Pfxparolası</span><span class="sxs-lookup"><span data-stu-id="e45c8-124">-PfxPassword</span></span>
<span data-ttu-id="e45c8-125">. Pfx sertifika dosyasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e45c8-125">Specifies the password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="e45c8-126">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="e45c8-126">-PfxPath</span></span>
<span data-ttu-id="e45c8-127">. Pfx sertifika dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e45c8-127">Specifies the path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="e45c8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e45c8-128">-ResourceGroupName</span></span>
<span data-ttu-id="e45c8-129">API yönetim dağıtımının olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e45c8-129">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="e45c8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e45c8-130">CommonParameters</span></span>
<span data-ttu-id="e45c8-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e45c8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e45c8-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e45c8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e45c8-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e45c8-133">INPUTS</span></span>

### <span data-ttu-id="e45c8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e45c8-134">System.String</span></span>

### <span data-ttu-id="e45c8-135">Microsoft. Azure. Commands. Apsananad. modeller. Psapsananagementhostnametype</span><span class="sxs-lookup"><span data-stu-id="e45c8-135">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType</span></span>

## <span data-ttu-id="e45c8-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e45c8-136">OUTPUTS</span></span>

### <span data-ttu-id="e45c8-137">Microsoft. Azure. Commands. Apsananad. modeller. Psapsananagementhostnamecertificate</span><span class="sxs-lookup"><span data-stu-id="e45c8-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="e45c8-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e45c8-138">NOTES</span></span>

## <span data-ttu-id="e45c8-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e45c8-139">RELATED LINKS</span></span>

[<span data-ttu-id="e45c8-140">Yeni-Azurermapımanagementhostnameconfiguration</span><span class="sxs-lookup"><span data-stu-id="e45c8-140">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)

[<span data-ttu-id="e45c8-141">Set-Azurermapımanagementhostnames</span><span class="sxs-lookup"><span data-stu-id="e45c8-141">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


