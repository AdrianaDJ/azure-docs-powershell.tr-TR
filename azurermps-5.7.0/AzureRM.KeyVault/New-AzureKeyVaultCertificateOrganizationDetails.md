---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateorganizationdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateOrganizationDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateOrganizationDetails.md
ms.openlocfilehash: 3ece43bb0c1d4c97c5d1956a25707c920215781c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594951"
---
# <span data-ttu-id="a93bd-101">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="a93bd-101">New-AzureKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="a93bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a93bd-102">SYNOPSIS</span></span>
<span data-ttu-id="a93bd-103">Bir bellek içi sertifika kuruluş ayrıntıları nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a93bd-103">Creates an in-memory certificate organization details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a93bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a93bd-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a93bd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a93bd-105">DESCRIPTION</span></span>
<span data-ttu-id="a93bd-106">**New-AzureKeyVaultCertificateOrganizationDetails** cmdlet 'i, bellek içi sertifika kuruluş ayrıntıları nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a93bd-106">The **New-AzureKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="a93bd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a93bd-107">EXAMPLES</span></span>

### <span data-ttu-id="a93bd-108">Örnek 1: kuruluş ayrıntıları nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a93bd-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzureKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="a93bd-109">İlk komut, Sertifika Yöneticisi Ayrıntılar nesnesi oluşturur ve $AdminDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a93bd-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="a93bd-110">İkinci komut, sertifika kuruluş ayrıntıları nesnesi oluşturur ve $OrgDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a93bd-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="a93bd-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a93bd-111">PARAMETERS</span></span>

### <span data-ttu-id="a93bd-112">-\Administrators ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="a93bd-112">-AdministratorDetails</span></span>
<span data-ttu-id="a93bd-113">Sertifika kuruluş yöneticilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a93bd-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a93bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a93bd-114">-DefaultProfile</span></span>
<span data-ttu-id="a93bd-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a93bd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a93bd-116">-ID</span><span class="sxs-lookup"><span data-stu-id="a93bd-116">-Id</span></span>
<span data-ttu-id="a93bd-117">Kuruluşun tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a93bd-117">Specifies the identifier for the organization.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93bd-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="a93bd-118">-Confirm</span></span>
<span data-ttu-id="a93bd-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a93bd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a93bd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a93bd-120">-WhatIf</span></span>
<span data-ttu-id="a93bd-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a93bd-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a93bd-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a93bd-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a93bd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a93bd-123">CommonParameters</span></span>
<span data-ttu-id="a93bd-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a93bd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a93bd-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a93bd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a93bd-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a93bd-126">INPUTS</span></span>

### <span data-ttu-id="a93bd-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a93bd-127">None</span></span>
<span data-ttu-id="a93bd-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a93bd-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a93bd-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a93bd-129">OUTPUTS</span></span>

### <span data-ttu-id="a93bd-130">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="a93bd-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="a93bd-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a93bd-131">NOTES</span></span>

## <span data-ttu-id="a93bd-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a93bd-132">RELATED LINKS</span></span>

[<span data-ttu-id="a93bd-133">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="a93bd-133">New-AzureKeyVaultCertificateAdministratorDetails</span></span>](./New-AzureKeyVaultCertificateAdministratorDetails.md)

