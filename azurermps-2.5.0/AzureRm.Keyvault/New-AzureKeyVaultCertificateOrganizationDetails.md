---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateorganizationdetails
schema: 2.0.0
ms.openlocfilehash: 76e0d37ac38c8b9799093ff3a4f4ea10c2fce2f4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939719"
---
# <span data-ttu-id="2e168-101">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="2e168-101">New-AzureKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="2e168-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e168-102">SYNOPSIS</span></span>
<span data-ttu-id="2e168-103">Bir bellek içi sertifika kuruluş ayrıntıları nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2e168-103">Creates an in-memory certificate organization details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e168-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e168-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e168-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e168-105">DESCRIPTION</span></span>
<span data-ttu-id="2e168-106">**New-AzureKeyVaultCertificateOrganizationDetails** cmdlet 'i, bellek içi sertifika kuruluş ayrıntıları nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2e168-106">The **New-AzureKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="2e168-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e168-107">EXAMPLES</span></span>

### <span data-ttu-id="2e168-108">Örnek 1: kuruluş ayrıntıları nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2e168-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzureKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="2e168-109">İlk komut, Sertifika Yöneticisi Ayrıntılar nesnesi oluşturur ve $AdminDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2e168-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="2e168-110">İkinci komut, sertifika kuruluş ayrıntıları nesnesi oluşturur ve $OrgDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2e168-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="2e168-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e168-111">PARAMETERS</span></span>

### <span data-ttu-id="2e168-112">-\Administrators ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="2e168-112">-AdministratorDetails</span></span>
<span data-ttu-id="2e168-113">Sertifika kuruluş yöneticilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e168-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="2e168-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e168-114">-DefaultProfile</span></span>
<span data-ttu-id="2e168-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2e168-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e168-116">-ID</span><span class="sxs-lookup"><span data-stu-id="2e168-116">-Id</span></span>
<span data-ttu-id="2e168-117">Kuruluşun tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e168-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="2e168-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="2e168-118">-Confirm</span></span>
<span data-ttu-id="2e168-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2e168-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e168-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e168-120">-WhatIf</span></span>
<span data-ttu-id="2e168-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2e168-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e168-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2e168-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e168-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e168-123">CommonParameters</span></span>
<span data-ttu-id="2e168-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e168-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e168-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e168-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e168-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e168-126">INPUTS</span></span>

## <span data-ttu-id="2e168-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e168-127">OUTPUTS</span></span>

### <span data-ttu-id="2e168-128">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="2e168-128">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="2e168-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e168-129">NOTES</span></span>

## <span data-ttu-id="2e168-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e168-130">RELATED LINKS</span></span>

[<span data-ttu-id="2e168-131">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="2e168-131">New-AzureKeyVaultCertificateAdministratorDetails</span></span>](./New-AzureKeyVaultCertificateAdministratorDetails.md)

