---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: ac9313611e5c228d33ea2dd473b0669e54ab1ca1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751661"
---
# <span data-ttu-id="16829-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="16829-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="16829-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16829-102">SYNOPSIS</span></span>
<span data-ttu-id="16829-103">Bir bellek içi sertifika kuruluş ayrıntıları nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16829-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="16829-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16829-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16829-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="16829-105">DESCRIPTION</span></span>
<span data-ttu-id="16829-106">**New-Azanahtarvaultcertificateorganizationdetail** cmdlet 'i, bellek içi sertifika kuruluş ayrıntıları nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16829-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="16829-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16829-107">EXAMPLES</span></span>

### <span data-ttu-id="16829-108">Örnek 1: kuruluş ayrıntıları nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="16829-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="16829-109">İlk komut, Sertifika Yöneticisi Ayrıntılar nesnesi oluşturur ve $AdminDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="16829-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="16829-110">İkinci komut, sertifika kuruluş ayrıntıları nesnesi oluşturur ve $OrgDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="16829-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="16829-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16829-111">PARAMETERS</span></span>

### <span data-ttu-id="16829-112">-\Administrators ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="16829-112">-AdministratorDetails</span></span>
<span data-ttu-id="16829-113">Sertifika kuruluş yöneticilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="16829-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="16829-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16829-114">-DefaultProfile</span></span>
<span data-ttu-id="16829-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="16829-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16829-116">-ID</span><span class="sxs-lookup"><span data-stu-id="16829-116">-Id</span></span>
<span data-ttu-id="16829-117">Kuruluşun tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16829-117">Specifies the identifier for the organization.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16829-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="16829-118">-Confirm</span></span>
<span data-ttu-id="16829-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="16829-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16829-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16829-120">-WhatIf</span></span>
<span data-ttu-id="16829-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="16829-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16829-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="16829-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16829-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16829-123">CommonParameters</span></span>
<span data-ttu-id="16829-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16829-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16829-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16829-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16829-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16829-126">INPUTS</span></span>

### <span data-ttu-id="16829-127">System. String</span><span class="sxs-lookup"><span data-stu-id="16829-127">System.String</span></span>

### <span data-ttu-id="16829-128">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificatetındetails, Microsoft. Azure. PowerShell. cmdlet. Keykasası, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="16829-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="16829-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16829-129">OUTPUTS</span></span>

### <span data-ttu-id="16829-130">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="16829-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="16829-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16829-131">NOTES</span></span>

## <span data-ttu-id="16829-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16829-132">RELATED LINKS</span></span>

[<span data-ttu-id="16829-133">Yeni-Aztuş Vaultcertificatetındetail</span><span class="sxs-lookup"><span data-stu-id="16829-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)

