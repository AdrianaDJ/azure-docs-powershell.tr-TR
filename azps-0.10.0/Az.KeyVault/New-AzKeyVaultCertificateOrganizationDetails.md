---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificateorganizationdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetails.md
ms.openlocfilehash: 76208f8d4c1b8b1b463ea5a0f24a4e34e7a82855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936665"
---
# <span data-ttu-id="19d53-101">New-AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="19d53-101">New-AzKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="19d53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19d53-102">SYNOPSIS</span></span>
<span data-ttu-id="19d53-103">Bir bellek içi sertifika kuruluş ayrıntıları nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="19d53-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="19d53-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19d53-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19d53-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="19d53-105">DESCRIPTION</span></span>
<span data-ttu-id="19d53-106">**New-Azanahtarvaultcertificateorganizationdetails** cmdlet 'i, bellek içi sertifika kuruluş ayrıntıları nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="19d53-106">The **New-AzKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="19d53-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19d53-107">EXAMPLES</span></span>

### <span data-ttu-id="19d53-108">Örnek 1: kuruluş ayrıntıları nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="19d53-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="19d53-109">İlk komut, Sertifika Yöneticisi Ayrıntılar nesnesi oluşturur ve $AdminDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="19d53-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="19d53-110">İkinci komut, sertifika kuruluş ayrıntıları nesnesi oluşturur ve $OrgDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="19d53-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="19d53-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19d53-111">PARAMETERS</span></span>

### <span data-ttu-id="19d53-112">-\Administrators ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="19d53-112">-AdministratorDetails</span></span>
<span data-ttu-id="19d53-113">Sertifika kuruluş yöneticilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="19d53-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19d53-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19d53-114">-DefaultProfile</span></span>
<span data-ttu-id="19d53-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="19d53-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d53-116">-ID</span><span class="sxs-lookup"><span data-stu-id="19d53-116">-Id</span></span>
<span data-ttu-id="19d53-117">Kuruluşun tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19d53-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="19d53-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="19d53-118">-Confirm</span></span>
<span data-ttu-id="19d53-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="19d53-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19d53-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19d53-120">-WhatIf</span></span>
<span data-ttu-id="19d53-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="19d53-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19d53-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="19d53-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19d53-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d53-123">CommonParameters</span></span>
<span data-ttu-id="19d53-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19d53-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d53-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19d53-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d53-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19d53-126">INPUTS</span></span>

### <span data-ttu-id="19d53-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="19d53-127">None</span></span>
<span data-ttu-id="19d53-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="19d53-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="19d53-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19d53-129">OUTPUTS</span></span>

### <span data-ttu-id="19d53-130">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="19d53-130">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="19d53-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19d53-131">NOTES</span></span>

## <span data-ttu-id="19d53-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19d53-132">RELATED LINKS</span></span>

[<span data-ttu-id="19d53-133">Yeni-Aztuş Vaultcertificate\administrators ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="19d53-133">New-AzKeyVaultCertificateAdministratorDetails</span></span>](./New-AzKeyVaultCertificateAdministratorDetails.md)

