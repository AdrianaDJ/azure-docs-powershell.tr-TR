---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A9C98F8F-90F2-4BF4-A234-31966FBB975B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
ms.openlocfilehash: ed1b4baac3d22789fe08964e4b4d31b53eee7223
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938652"
---
# <span data-ttu-id="34f14-101">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="34f14-101">Get-AzBatchCertificate</span></span>

## <span data-ttu-id="34f14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34f14-102">SYNOPSIS</span></span>
<span data-ttu-id="34f14-103">Sertifikaları bir toplu Iş hesabında alır.</span><span class="sxs-lookup"><span data-stu-id="34f14-103">Gets the certificates in a Batch account.</span></span>

## <span data-ttu-id="34f14-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34f14-104">SYNTAX</span></span>

### <span data-ttu-id="34f14-105">ODataFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34f14-105">ODataFilter (Default)</span></span>
```
Get-AzBatchCertificate [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34f14-106">İziyle</span><span class="sxs-lookup"><span data-stu-id="34f14-106">Thumbprint</span></span>
```
Get-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String> [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34f14-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="34f14-107">DESCRIPTION</span></span>
<span data-ttu-id="34f14-108">**Get-AzBatchCertificate** cmdlet 'ı, Azure toplu hesabındaki sertifikaları, *batchcontext* parametresinin belirttiği sertifikaları alır.</span><span class="sxs-lookup"><span data-stu-id="34f14-108">The **Get-AzBatchCertificate** cmdlet gets the certificates in the Azure Batch account that the *BatchContext* parameter specifies.</span></span>
<span data-ttu-id="34f14-109">Belirli bir sertifika edinmek için, *Thumbprintalgorithm* ve *parmak izi* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="34f14-109">To obtain a particular certificate, specify the *ThumbprintAlgorithm* and *Thumbprint* parameters.</span></span>
<span data-ttu-id="34f14-110">Açık bir veri Protokolü (OData) filtresiyle eşleşen sertifikaların alınacağı *filtre* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="34f14-110">Specify the *Filter* parameter to get the certificates that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="34f14-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34f14-111">EXAMPLES</span></span>

### <span data-ttu-id="34f14-112">Örnek 1: parmak iziyle sertifika alma</span><span class="sxs-lookup"><span data-stu-id="34f14-112">Example 1: Get a certificate by thumbprint</span></span>
```
PS C:\>Get-AzBatchCertificate -ThumbprintAlgorithm "sha1" - Thumbprint "C1E494A415149C5F211C4778B52F2E834A07247C" -BatchContext $Context
Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=C1E494A415149C5F211C4778B52F2E834A07247
C) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="34f14-113">Bu komut belirtilen parmak izine sahip tek bir sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="34f14-113">This command gets a single certificate that has the specified thumbprint.</span></span>
<span data-ttu-id="34f14-114">Sertifika parmak izi algoritması SHA1.</span><span class="sxs-lookup"><span data-stu-id="34f14-114">The certificate thumbprint algorithm is sha1.</span></span>

### <span data-ttu-id="34f14-115">Örnek 2: filtrelenmiş Sertifikalar alma</span><span class="sxs-lookup"><span data-stu-id="34f14-115">Example 2: Get filtered certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context
Thumbprint                  : 025b351b087a084c5067f5e71eff8591970323f9
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=025b351b087a084c5067f5e71eff8591970323f9) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:17 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAyMB4XDTE1MTAwMjE2MjkxNFoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDIwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAJxagvVrlnKfv6hfzSiFJUkdGkPjC3tFiKebK6IaeHzesFdFfupXUE
wT0xOWh9xwa3OVkPECEc/u1sw3iVX/J4AODiwzmOWutoVRpWjxGFpgw9+dPvXMjs/Ue7JL7ag3siHs5EcarW91qKbgtko6i/r4emaRyk60U93TrbWQAWJ9AgMBAAGjS
zBJMEcGA1UdAQRAMD6AEAdqsOpyeXF/uDe7ZGKeez+hGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMoIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAA4GBAC0MaAem
6ByyURFvGnFZyjEepjXC5wcaGq+gguDFe8rG88ceig1ZqewdcmC1y4p05uBhbmETbYVWzJarNsHYq2LTihi4t2J4jt2YVYz/IRdUB82iaFFbJRSPrN+6xD3KM2lve5N
4OjtlZAdiXiSUYFf3I6ypberUsAdba3QQajCN
DeleteCertificateError      : 

Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=c1e494a415149c5f211c4778b52f2e834a07247c) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="34f14-116">Bu komut, etkin durumdaki tüm sertifikaları toplu Iş hesabından alır.</span><span class="sxs-lookup"><span data-stu-id="34f14-116">This command gets all certificates in the active state from the Batch account.</span></span>
<span data-ttu-id="34f14-117">*Filter* parametresi durumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="34f14-117">The *Filter* parameter specifies the state.</span></span>

## <span data-ttu-id="34f14-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34f14-118">PARAMETERS</span></span>

### <span data-ttu-id="34f14-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="34f14-119">-BatchContext</span></span>
<span data-ttu-id="34f14-120">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34f14-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="34f14-121">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="34f14-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="34f14-122">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="34f14-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="34f14-123">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="34f14-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="34f14-124">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="34f14-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34f14-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f14-125">-DefaultProfile</span></span>
<span data-ttu-id="34f14-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34f14-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34f14-127">-Filtre</span><span class="sxs-lookup"><span data-stu-id="34f14-127">-Filter</span></span>
<span data-ttu-id="34f14-128">Bir OData filtre yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="34f14-128">Specifies an OData filter clause.</span></span>
<span data-ttu-id="34f14-129">Bu parametreyi belirtirseniz, bu cmdlet filtreyle eşleşen sertifikaları alır.</span><span class="sxs-lookup"><span data-stu-id="34f14-129">If you specify this parameter, this cmdlet gets the certificates that match the filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f14-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="34f14-130">-MaxCount</span></span>
<span data-ttu-id="34f14-131">Döndürülecek en fazla sertifika sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34f14-131">Specifies the maximum number of certificates to return.</span></span>
<span data-ttu-id="34f14-132">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="34f14-132">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="34f14-133">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="34f14-133">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f14-134">-Select</span><span class="sxs-lookup"><span data-stu-id="34f14-134">-Select</span></span>
<span data-ttu-id="34f14-135">Bir OData select yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="34f14-135">Specifies an OData select clause.</span></span>
<span data-ttu-id="34f14-136">Tüm nesne özellikleri yerine belirli özellikleri almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="34f14-136">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="34f14-137">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="34f14-137">-Thumbprint</span></span>
<span data-ttu-id="34f14-138">Bu cmdlet 'in aldığı sertifikanın parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34f14-138">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34f14-139">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="34f14-139">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="34f14-140">*Parmak izi* parametresini türetmek için kullanılan algoritmayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="34f14-140">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="34f14-141">Şu anda tek geçerli değer SHA1 ' dır.</span><span class="sxs-lookup"><span data-stu-id="34f14-141">Currently, the only valid value is sha1.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34f14-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f14-142">CommonParameters</span></span>
<span data-ttu-id="34f14-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34f14-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f14-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34f14-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f14-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34f14-145">INPUTS</span></span>

### <span data-ttu-id="34f14-146">System. String</span><span class="sxs-lookup"><span data-stu-id="34f14-146">System.String</span></span>

### <span data-ttu-id="34f14-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="34f14-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="34f14-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34f14-148">OUTPUTS</span></span>

### <span data-ttu-id="34f14-149">Microsoft.Azure.Commands.Batch. Modeller. Pscercertificate</span><span class="sxs-lookup"><span data-stu-id="34f14-149">Microsoft.Azure.Commands.Batch.Models.PSCertificate</span></span>

## <span data-ttu-id="34f14-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34f14-150">NOTES</span></span>

## <span data-ttu-id="34f14-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34f14-151">RELATED LINKS</span></span>

[<span data-ttu-id="34f14-152">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="34f14-152">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="34f14-153">Yeni-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="34f14-153">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="34f14-154">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="34f14-154">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="34f14-155">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="34f14-155">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

