---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: 39deb08468912bf727198ec4f90f5f4f0680941f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278662"
---
# <span data-ttu-id="802c1-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="802c1-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="802c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="802c1-102">SYNOPSIS</span></span>
<span data-ttu-id="802c1-103">Bir bellek içi Sertifika Yöneticisi Ayrıntılar nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="802c1-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="802c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="802c1-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="802c1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="802c1-105">DESCRIPTION</span></span>
<span data-ttu-id="802c1-106">**New-Azanahtarvaultcertificate\administrators ayrıntı** cmdlet 'i, bellek içi Sertifika Yöneticisi Ayrıntılar nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="802c1-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="802c1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="802c1-107">EXAMPLES</span></span>

### <span data-ttu-id="802c1-108">Örnek 1: Sertifika Yöneticisi Ayrıntılar nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="802c1-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="802c1-109">Bu komut, bir bellek içi Sertifika Yöneticisi Ayrıntılar nesnesi oluşturur ve $AdminDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="802c1-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="802c1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="802c1-110">PARAMETERS</span></span>

### <span data-ttu-id="802c1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="802c1-111">-DefaultProfile</span></span>
<span data-ttu-id="802c1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="802c1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="802c1-113">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="802c1-113">-EmailAddress</span></span>
<span data-ttu-id="802c1-114">Sertifika yöneticisinin e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="802c1-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="802c1-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="802c1-115">-FirstName</span></span>
<span data-ttu-id="802c1-116">Sertifika yöneticisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="802c1-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="802c1-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="802c1-117">-LastName</span></span>
<span data-ttu-id="802c1-118">Sertifika yöneticisinin soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="802c1-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="802c1-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="802c1-119">-PhoneNumber</span></span>
<span data-ttu-id="802c1-120">Sertifika yöneticisinin telefon numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="802c1-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="802c1-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="802c1-121">-Confirm</span></span>
<span data-ttu-id="802c1-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="802c1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="802c1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="802c1-123">-WhatIf</span></span>
<span data-ttu-id="802c1-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="802c1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="802c1-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="802c1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="802c1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="802c1-126">CommonParameters</span></span>
<span data-ttu-id="802c1-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="802c1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="802c1-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="802c1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="802c1-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="802c1-129">INPUTS</span></span>

### <span data-ttu-id="802c1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="802c1-130">System.String</span></span>

## <span data-ttu-id="802c1-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="802c1-131">OUTPUTS</span></span>

### <span data-ttu-id="802c1-132">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificate\administrators ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="802c1-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="802c1-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="802c1-133">NOTES</span></span>

## <span data-ttu-id="802c1-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="802c1-134">RELATED LINKS</span></span>

[<span data-ttu-id="802c1-135">Yeni-Aztuş Vaultcertificateorganizationdetail</span><span class="sxs-lookup"><span data-stu-id="802c1-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

