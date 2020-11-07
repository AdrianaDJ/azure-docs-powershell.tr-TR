---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateattribute
schema: 2.0.0
ms.openlocfilehash: 9f7c08f42026c6cc5d321ae78687a903c8393904
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938817"
---
# <span data-ttu-id="432db-101">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="432db-101">Set-AzureKeyVaultCertificateAttribute</span></span>

## <span data-ttu-id="432db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="432db-102">SYNOPSIS</span></span>
<span data-ttu-id="432db-103">Sertifikanın düzenlenebilir özniteliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="432db-103">Modifies editable attributes of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="432db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="432db-104">SYNTAX</span></span>

```
Set-AzureKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="432db-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="432db-105">DESCRIPTION</span></span>
<span data-ttu-id="432db-106">**Set-AzureKeyVaultCertificateAttribute** cmdlet 'i, bir sertifikanın düzenlenebilir özniteliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="432db-106">The **Set-AzureKeyVaultCertificateAttribute** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="432db-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="432db-107">EXAMPLES</span></span>

### <span data-ttu-id="432db-108">Örnek 1: sertifikayla ilişkili etiketleri değiştirme</span><span class="sxs-lookup"><span data-stu-id="432db-108">Example 1: Modify the tags associated with a certificate</span></span>
```
PS C:\>$Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Set-AzureKeyVaultCertificateAttribute -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags
PS C:\> Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : "TestCert01"
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                5A2EF60501F241D6A4336841B36FEA41

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                A565D568082FEE2BE33B356ECC3703C2E9886555

Id          : https://ContosoKV01.vault.azure.net:443/certificates/tt02
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/tt02
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/tt02
Thumbprint  : A565D568082FEE2BE33B356ECC3703C2E9886555
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="432db-109">İlk komut $Tags değişkenine anahtar/değer çiftleri dizisi atar.</span><span class="sxs-lookup"><span data-stu-id="432db-109">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="432db-110">İkinci komut, TestCert01 adındaki sertifikanın etiket değerini $Tags olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="432db-110">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

<span data-ttu-id="432db-111">Final komutu, işlemi doğrulamak için Get-AzureKeyVaultCertificate cmdlet 'ini kullanarak TestCert01 sertifikasını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="432db-111">The final command displays the TestCert01 certificate by using the Get-AzureKeyVaultCertificate cmdlet to verify the operation.</span></span>

## <span data-ttu-id="432db-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="432db-112">PARAMETERS</span></span>

### <span data-ttu-id="432db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="432db-113">-DefaultProfile</span></span>
<span data-ttu-id="432db-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="432db-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="432db-115">-Enable</span><span class="sxs-lookup"><span data-stu-id="432db-115">-Enable</span></span>
<span data-ttu-id="432db-116">Sertifikanın etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="432db-116">Indicates whether to enable or disable a certificate.</span></span>
<span data-ttu-id="432db-117">Etkinleştirmek $False veya devre dışı bırakmak için $True belirtin.</span><span class="sxs-lookup"><span data-stu-id="432db-117">Specify $True to enable or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="432db-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="432db-118">-Name</span></span>
<span data-ttu-id="432db-119">Değiştirilecek sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="432db-119">Specifies the name of the certificate to modify.</span></span> <span data-ttu-id="432db-120">Bu cmdlet, bir sertifikanın FQDN 'sini Anahtar Kasası adına, şu anda seçtiğiniz ortama, sertifika adına ve sertifika sürümüne göre oluşturur.</span><span class="sxs-lookup"><span data-stu-id="432db-120">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="432db-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="432db-121">-PassThru</span></span>
<span data-ttu-id="432db-122">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="432db-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="432db-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="432db-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="432db-124">Etiketli</span><span class="sxs-lookup"><span data-stu-id="432db-124">-Tag</span></span>
<span data-ttu-id="432db-125">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="432db-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="432db-126">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="432db-126">For example:</span></span>

<span data-ttu-id="432db-127">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="432db-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="432db-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="432db-128">-VaultName</span></span>
<span data-ttu-id="432db-129">Bu cmdlet 'in sertifikayı değiştirdiği tuş Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="432db-129">Specifies the key vault name in which this cmdlet modifies a certificate.</span></span>
<span data-ttu-id="432db-130">Bu cmdlet, ad ve seçili durumdaki ortamı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="432db-130">This cmdlet constructs the FQDN of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="432db-131">-Version</span><span class="sxs-lookup"><span data-stu-id="432db-131">-Version</span></span>
<span data-ttu-id="432db-132">Sertifikanın sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="432db-132">Specifies the version of a certificate.</span></span>
<span data-ttu-id="432db-133">Bu cmdlet, bir sertifikanın FQDN 'sini Anahtar Kasası adına, şu anda seçtiğiniz ortama, sertifika adına ve sertifika sürümüne göre oluşturur.</span><span class="sxs-lookup"><span data-stu-id="432db-133">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="432db-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="432db-134">-Confirm</span></span>
<span data-ttu-id="432db-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="432db-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="432db-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="432db-136">-WhatIf</span></span>
<span data-ttu-id="432db-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="432db-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="432db-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="432db-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="432db-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="432db-139">CommonParameters</span></span>
<span data-ttu-id="432db-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="432db-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="432db-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="432db-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="432db-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="432db-142">INPUTS</span></span>

## <span data-ttu-id="432db-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="432db-143">OUTPUTS</span></span>

### <span data-ttu-id="432db-144">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="432db-144">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="432db-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="432db-145">NOTES</span></span>

## <span data-ttu-id="432db-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="432db-146">RELATED LINKS</span></span>

[<span data-ttu-id="432db-147">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="432db-147">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)
