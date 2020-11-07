---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
ms.openlocfilehash: 8753b3ad76e9b68963e523fdff2a3c505147bc19
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753839"
---
# <span data-ttu-id="c67d0-101">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="c67d0-101">Get-AzWebAppCertificate</span></span>

## <span data-ttu-id="c67d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c67d0-102">SYNOPSIS</span></span>
<span data-ttu-id="c67d0-103">Bir Azure Web App sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="c67d0-103">Gets an Azure Web App certificate.</span></span>

## <span data-ttu-id="c67d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c67d0-104">SYNTAX</span></span>

```
Get-AzWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c67d0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c67d0-105">DESCRIPTION</span></span>
<span data-ttu-id="c67d0-106">**Get-AzWebAppCertificate** cmdlet 'i, belirli bir kaynak grubuyla Ilişkili Azure Web App sertifikaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c67d0-106">The **Get-AzWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="c67d0-107">Sertifika parmak izini biliyorsanız, belirli bir sertifika hakkında bilgi almak için bu cmdlet 'i de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c67d0-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="c67d0-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c67d0-108">EXAMPLES</span></span>

### <span data-ttu-id="c67d0-109">Örnek 1: kaynak grubundaki Web uygulaması sertifikalarını alma</span><span class="sxs-lookup"><span data-stu-id="c67d0-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="c67d0-110">Bu komut, ContosoResourceGroup kaynak grubuyla ilişkili karşıya yüklenen Web uygulaması sertifikaları hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="c67d0-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="c67d0-111">Örnek 2: belirtilen Web uygulaması sertifikasını alma</span><span class="sxs-lookup"><span data-stu-id="c67d0-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="c67d0-112">Bu komut, E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 parmak iziyle ContosoResourceGroup Web App sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="c67d0-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="c67d0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c67d0-113">PARAMETERS</span></span>

### <span data-ttu-id="c67d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c67d0-114">-DefaultProfile</span></span>
<span data-ttu-id="c67d0-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c67d0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c67d0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c67d0-116">-ResourceGroupName</span></span>
<span data-ttu-id="c67d0-117">Sertifikanın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c67d0-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="c67d0-118">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="c67d0-118">-Thumbprint</span></span>
<span data-ttu-id="c67d0-119">Sertifikanın benzersiz tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c67d0-119">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="c67d0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c67d0-120">CommonParameters</span></span>
<span data-ttu-id="c67d0-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c67d0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c67d0-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c67d0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c67d0-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c67d0-123">INPUTS</span></span>

### <span data-ttu-id="c67d0-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c67d0-124">None</span></span>

## <span data-ttu-id="c67d0-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c67d0-125">OUTPUTS</span></span>

### <span data-ttu-id="c67d0-126">Microsoft. Azure. Commands. WebApps. modeller. WebApp. Pscercertificate</span><span class="sxs-lookup"><span data-stu-id="c67d0-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="c67d0-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c67d0-127">NOTES</span></span>

## <span data-ttu-id="c67d0-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c67d0-128">RELATED LINKS</span></span>

[<span data-ttu-id="c67d0-129">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="c67d0-129">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)


