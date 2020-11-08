---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: 39deb08468912bf727198ec4f90f5f4f0680941f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109985"
---
# <span data-ttu-id="70c82-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="70c82-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="70c82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70c82-102">SYNOPSIS</span></span>
<span data-ttu-id="70c82-103">Bir bellek içi Sertifika Yöneticisi Ayrıntılar nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70c82-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="70c82-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70c82-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70c82-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="70c82-105">DESCRIPTION</span></span>
<span data-ttu-id="70c82-106">**New-Azanahtarvaultcertificate\administrators ayrıntı** cmdlet 'i, bellek içi Sertifika Yöneticisi Ayrıntılar nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70c82-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="70c82-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70c82-107">EXAMPLES</span></span>

### <span data-ttu-id="70c82-108">Örnek 1: Sertifika Yöneticisi Ayrıntılar nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="70c82-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="70c82-109">Bu komut, bir bellek içi Sertifika Yöneticisi Ayrıntılar nesnesi oluşturur ve $AdminDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="70c82-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="70c82-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70c82-110">PARAMETERS</span></span>

### <span data-ttu-id="70c82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c82-111">-DefaultProfile</span></span>
<span data-ttu-id="70c82-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="70c82-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70c82-113">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="70c82-113">-EmailAddress</span></span>
<span data-ttu-id="70c82-114">Sertifika yöneticisinin e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="70c82-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="70c82-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="70c82-115">-FirstName</span></span>
<span data-ttu-id="70c82-116">Sertifika yöneticisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="70c82-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="70c82-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="70c82-117">-LastName</span></span>
<span data-ttu-id="70c82-118">Sertifika yöneticisinin soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="70c82-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="70c82-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="70c82-119">-PhoneNumber</span></span>
<span data-ttu-id="70c82-120">Sertifika yöneticisinin telefon numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="70c82-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="70c82-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="70c82-121">-Confirm</span></span>
<span data-ttu-id="70c82-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="70c82-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70c82-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70c82-123">-WhatIf</span></span>
<span data-ttu-id="70c82-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="70c82-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70c82-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="70c82-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70c82-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c82-126">CommonParameters</span></span>
<span data-ttu-id="70c82-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70c82-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c82-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="70c82-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c82-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70c82-129">INPUTS</span></span>

### <span data-ttu-id="70c82-130">System. String</span><span class="sxs-lookup"><span data-stu-id="70c82-130">System.String</span></span>

## <span data-ttu-id="70c82-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70c82-131">OUTPUTS</span></span>

### <span data-ttu-id="70c82-132">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificate\administrators ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="70c82-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="70c82-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70c82-133">NOTES</span></span>

## <span data-ttu-id="70c82-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70c82-134">RELATED LINKS</span></span>

[<span data-ttu-id="70c82-135">Yeni-Aztuş Vaultcertificateorganizationdetail</span><span class="sxs-lookup"><span data-stu-id="70c82-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

