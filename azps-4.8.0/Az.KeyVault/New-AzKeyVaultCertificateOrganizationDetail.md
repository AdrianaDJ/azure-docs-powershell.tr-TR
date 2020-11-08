---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: 56b956aa8a65c4586859325f110f3ce593b2289c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267212"
---
# <span data-ttu-id="ba5e4-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="ba5e4-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="ba5e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba5e4-102">SYNOPSIS</span></span>
<span data-ttu-id="ba5e4-103">Bir bellek içi sertifika kuruluş ayrıntıları nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ba5e4-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="ba5e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba5e4-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba5e4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba5e4-105">DESCRIPTION</span></span>
<span data-ttu-id="ba5e4-106">**New-Azanahtarvaultcertificateorganizationdetail** cmdlet 'i, bellek içi sertifika kuruluş ayrıntıları nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ba5e4-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="ba5e4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba5e4-107">EXAMPLES</span></span>

### <span data-ttu-id="ba5e4-108">Örnek 1: kuruluş ayrıntıları nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="ba5e4-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="ba5e4-109">İlk komut, Sertifika Yöneticisi Ayrıntılar nesnesi oluşturur ve $AdminDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ba5e4-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="ba5e4-110">İkinci komut, sertifika kuruluş ayrıntıları nesnesi oluşturur ve $OrgDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ba5e4-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="ba5e4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba5e4-111">PARAMETERS</span></span>

### <span data-ttu-id="ba5e4-112">-\Administrators ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="ba5e4-112">-AdministratorDetails</span></span>
<span data-ttu-id="ba5e4-113">Sertifika kuruluş yöneticilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba5e4-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="ba5e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba5e4-114">-DefaultProfile</span></span>
<span data-ttu-id="ba5e4-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ba5e4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba5e4-116">-ID</span><span class="sxs-lookup"><span data-stu-id="ba5e4-116">-Id</span></span>
<span data-ttu-id="ba5e4-117">Kuruluşun tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba5e4-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="ba5e4-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="ba5e4-118">-Confirm</span></span>
<span data-ttu-id="ba5e4-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ba5e4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba5e4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba5e4-120">-WhatIf</span></span>
<span data-ttu-id="ba5e4-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba5e4-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba5e4-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ba5e4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba5e4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba5e4-123">CommonParameters</span></span>
<span data-ttu-id="ba5e4-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba5e4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba5e4-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ba5e4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba5e4-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba5e4-126">INPUTS</span></span>

### <span data-ttu-id="ba5e4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ba5e4-127">System.String</span></span>

### <span data-ttu-id="ba5e4-128">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificatetındetails, Microsoft. Azure. PowerShell. cmdlet. Keykasası, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ba5e4-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ba5e4-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba5e4-129">OUTPUTS</span></span>

### <span data-ttu-id="ba5e4-130">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="ba5e4-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="ba5e4-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba5e4-131">NOTES</span></span>

## <span data-ttu-id="ba5e4-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba5e4-132">RELATED LINKS</span></span>

[<span data-ttu-id="ba5e4-133">Yeni-Aztuş Vaultcertificatetındetail</span><span class="sxs-lookup"><span data-stu-id="ba5e4-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)

