---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: dd87a5b9abf6126fee71bbc308ec3a985c9da9de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765168"
---
# <span data-ttu-id="48d9b-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="48d9b-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="48d9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="48d9b-103">Anahtar kasasından sertifika alır.</span><span class="sxs-lookup"><span data-stu-id="48d9b-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48d9b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48d9b-104">SYNTAX</span></span>

### <span data-ttu-id="48d9b-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="48d9b-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="48d9b-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="48d9b-106">ByCertificateName</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48d9b-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="48d9b-107">ByCertificateVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48d9b-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="48d9b-108">ByDeletedCertificates</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48d9b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="48d9b-109">DESCRIPTION</span></span>
<span data-ttu-id="48d9b-110">**Get-AzureKeyVaultCertificate** cmdlet 'ı, Azure Anahtar Kasası 'ndaki anahtar kasasından belirtilen sertifikayı veya sertifika sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="48d9b-110">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="48d9b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48d9b-111">EXAMPLES</span></span>

### <span data-ttu-id="48d9b-112">Örnek 1: sertifika alma</span><span class="sxs-lookup"><span data-stu-id="48d9b-112">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="48d9b-113">Bu komut, ContosoKV01 adındaki anahtar kasasına TestCert01 adındaki sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="48d9b-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="48d9b-114">Örnek 2: Bu anahtar kasası için silinmiş ancak temizlenmiş tüm sertifikaları edinin.</span><span class="sxs-lookup"><span data-stu-id="48d9b-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="48d9b-115">Bu komut, contoso adlı Anahtar Kasası 'nda, önceden silinen ancak temizlenmemayan tüm sertifikaları alır.</span><span class="sxs-lookup"><span data-stu-id="48d9b-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="48d9b-116">Örnek 3: silinen, ancak bu Anahtar Kasası için temizlenmiş olan sertifikayı alma.</span><span class="sxs-lookup"><span data-stu-id="48d9b-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="48d9b-117">Bu komut, contoso adlı Anahtar Kasası 'nda, önceden silinmiş ancak temizlenmeden önce ' MyCert ' adındaki sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="48d9b-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="48d9b-118">Bu komut, silme tarihi ve bu silinmiş sertifikanın zamanlanmış temizleme tarihi gibi meta verileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="48d9b-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="48d9b-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48d9b-119">PARAMETERS</span></span>

### <span data-ttu-id="48d9b-120">-Includeversions</span><span class="sxs-lookup"><span data-stu-id="48d9b-120">-IncludeVersions</span></span>
<span data-ttu-id="48d9b-121">Bu işlemin sertifikanın tüm sürümlerini aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="48d9b-121">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByCertificateVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d9b-122">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="48d9b-122">-InRemovedState</span></span>
<span data-ttu-id="48d9b-123">Çıktıya önceden silinmiş sertifikaların eklenip eklenmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="48d9b-123">Specifies whether to include previously deleted certificates in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedCertificates
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d9b-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="48d9b-124">-Name</span></span>
<span data-ttu-id="48d9b-125">Alınacak sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="48d9b-125">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName, ByCertificateVersions
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedCertificates
Aliases: CertificateName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48d9b-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="48d9b-126">-VaultName</span></span>
<span data-ttu-id="48d9b-127">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="48d9b-127">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48d9b-128">-Version</span><span class="sxs-lookup"><span data-stu-id="48d9b-128">-Version</span></span>
<span data-ttu-id="48d9b-129">Sertifikanın sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="48d9b-129">Specifies the version of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: CertificateVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48d9b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d9b-130">-DefaultProfile</span></span>
<span data-ttu-id="48d9b-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="48d9b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48d9b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d9b-132">CommonParameters</span></span>
<span data-ttu-id="48d9b-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48d9b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d9b-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48d9b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d9b-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48d9b-135">INPUTS</span></span>

## <span data-ttu-id="48d9b-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48d9b-136">OUTPUTS</span></span>

### <span data-ttu-id="48d9b-137">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Keykasa. modeller. Certificateıdentityıtem]</span><span class="sxs-lookup"><span data-stu-id="48d9b-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="48d9b-138">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="48d9b-138">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="48d9b-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48d9b-139">NOTES</span></span>

## <span data-ttu-id="48d9b-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48d9b-140">RELATED LINKS</span></span>

[<span data-ttu-id="48d9b-141">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="48d9b-141">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="48d9b-142">İçeri aktarma-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="48d9b-142">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="48d9b-143">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="48d9b-143">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="48d9b-144">Geri al-AzureKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="48d9b-144">Undo-AzureKeyVaultSecretCertificate</span></span>](./Undo-AzureKeyVaultSecretCertificate.md)
