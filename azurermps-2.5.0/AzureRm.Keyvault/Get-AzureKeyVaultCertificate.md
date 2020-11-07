---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: ed52e229f114666782cb24388db585fd08fa685b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939928"
---
# <span data-ttu-id="fb579-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fb579-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="fb579-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb579-102">SYNOPSIS</span></span>
<span data-ttu-id="fb579-103">Anahtar kasasından sertifika alır.</span><span class="sxs-lookup"><span data-stu-id="fb579-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb579-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb579-104">SYNTAX</span></span>

### <span data-ttu-id="fb579-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fb579-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb579-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="fb579-106">ByCertificateName</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb579-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="fb579-107">ByCertificateVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb579-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="fb579-108">ByDeletedCertificates</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb579-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb579-109">DESCRIPTION</span></span>
<span data-ttu-id="fb579-110">**Get-AzureKeyVaultCertificate** cmdlet 'ı, Azure Anahtar Kasası 'ndaki anahtar kasasından belirtilen sertifikayı veya sertifika sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="fb579-110">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="fb579-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb579-111">EXAMPLES</span></span>

### <span data-ttu-id="fb579-112">Örnek 1: sertifika alma</span><span class="sxs-lookup"><span data-stu-id="fb579-112">Example 1: Get a certificate</span></span>
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

<span data-ttu-id="fb579-113">Bu komut, ContosoKV01 adındaki anahtar kasasına TestCert01 adındaki sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="fb579-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="fb579-114">Örnek 2: Bu anahtar kasası için silinmiş ancak temizlenmiş tüm sertifikaları edinin.</span><span class="sxs-lookup"><span data-stu-id="fb579-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="fb579-115">Bu komut, contoso adlı Anahtar Kasası 'nda, önceden silinen ancak temizlenmemayan tüm sertifikaları alır.</span><span class="sxs-lookup"><span data-stu-id="fb579-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="fb579-116">Örnek 3: silinen, ancak bu Anahtar Kasası için temizlenmiş olan sertifikayı alma.</span><span class="sxs-lookup"><span data-stu-id="fb579-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="fb579-117">Bu komut, contoso adlı Anahtar Kasası 'nda, önceden silinmiş ancak temizlenmeden önce ' MyCert ' adındaki sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="fb579-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="fb579-118">Bu komut, silme tarihi ve bu silinmiş sertifikanın zamanlanmış temizleme tarihi gibi meta verileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="fb579-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="fb579-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb579-119">PARAMETERS</span></span>

### <span data-ttu-id="fb579-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb579-120">-DefaultProfile</span></span>
<span data-ttu-id="fb579-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fb579-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb579-122">-Includeversions</span><span class="sxs-lookup"><span data-stu-id="fb579-122">-IncludeVersions</span></span>
<span data-ttu-id="fb579-123">Bu işlemin sertifikanın tüm sürümlerini aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb579-123">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb579-124">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="fb579-124">-InRemovedState</span></span>
<span data-ttu-id="fb579-125">Çıkışta önceden silinmiş sertifikaların eklenip eklenmeyeceğini belirtir</span><span class="sxs-lookup"><span data-stu-id="fb579-125">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedCertificates
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb579-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb579-126">-Name</span></span>
<span data-ttu-id="fb579-127">Alınacak sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb579-127">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName, ByCertificateVersions
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedCertificates
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb579-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fb579-128">-VaultName</span></span>
<span data-ttu-id="fb579-129">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb579-129">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="fb579-130">-Version</span><span class="sxs-lookup"><span data-stu-id="fb579-130">-Version</span></span>
<span data-ttu-id="fb579-131">Sertifikanın sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb579-131">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb579-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb579-132">CommonParameters</span></span>
<span data-ttu-id="fb579-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb579-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb579-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb579-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb579-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb579-135">INPUTS</span></span>

## <span data-ttu-id="fb579-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb579-136">OUTPUTS</span></span>

### <span data-ttu-id="fb579-137">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Keykasa. modeller. Certificateıdentityıtem]</span><span class="sxs-lookup"><span data-stu-id="fb579-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="fb579-138">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fb579-138">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="fb579-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb579-139">NOTES</span></span>

## <span data-ttu-id="fb579-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb579-140">RELATED LINKS</span></span>

[<span data-ttu-id="fb579-141">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fb579-141">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="fb579-142">İçeri aktarma-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fb579-142">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="fb579-143">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fb579-143">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)


