---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
ms.openlocfilehash: d7fbd87a436b9d0ea2fd0d311e19dc3df5bb8dda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592151"
---
# <span data-ttu-id="1d2ff-101">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="1d2ff-101">Get-AzureRmWebAppCertificate</span></span>

## <span data-ttu-id="1d2ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d2ff-102">SYNOPSIS</span></span>
<span data-ttu-id="1d2ff-103">Bir Azure Web App sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-103">Gets an Azure Web App certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d2ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d2ff-104">SYNTAX</span></span>

```
Get-AzureRmWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d2ff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d2ff-105">DESCRIPTION</span></span>
<span data-ttu-id="1d2ff-106">**Get-AzureRmWebAppCertificate** cmdlet 'i, belirli bir kaynak grubuyla Ilişkili Azure Web App sertifikaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-106">The **Get-AzureRmWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="1d2ff-107">Sertifika parmak izini biliyorsanız, belirli bir sertifika hakkında bilgi almak için bu cmdlet 'i de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="1d2ff-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d2ff-108">EXAMPLES</span></span>

### <span data-ttu-id="1d2ff-109">Örnek 1: kaynak grubundaki Web uygulaması sertifikalarını alma</span><span class="sxs-lookup"><span data-stu-id="1d2ff-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="1d2ff-110">Bu komut, ContosoResourceGroup kaynak grubuyla ilişkili karşıya yüklenen Web uygulaması sertifikaları hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="1d2ff-111">Örnek 2: belirtilen Web uygulaması sertifikasını alma</span><span class="sxs-lookup"><span data-stu-id="1d2ff-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="1d2ff-112">Bu komut, E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 parmak iziyle ContosoResourceGroup Web App sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="1d2ff-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d2ff-113">PARAMETERS</span></span>

### <span data-ttu-id="1d2ff-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d2ff-114">-ResourceGroupName</span></span>
<span data-ttu-id="1d2ff-115">Sertifikanın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-115">Specifies the name of the resource group that the certificate is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d2ff-116">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="1d2ff-116">-Thumbprint</span></span>
<span data-ttu-id="1d2ff-117">Sertifikanın benzersiz tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-117">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d2ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d2ff-118">-DefaultProfile</span></span>
<span data-ttu-id="1d2ff-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d2ff-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d2ff-120">CommonParameters</span></span>
<span data-ttu-id="1d2ff-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d2ff-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d2ff-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d2ff-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d2ff-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d2ff-123">INPUTS</span></span>

## <span data-ttu-id="1d2ff-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d2ff-124">OUTPUTS</span></span>

## <span data-ttu-id="1d2ff-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d2ff-125">NOTES</span></span>

## <span data-ttu-id="1d2ff-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d2ff-126">RELATED LINKS</span></span>

[<span data-ttu-id="1d2ff-127">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="1d2ff-127">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)


