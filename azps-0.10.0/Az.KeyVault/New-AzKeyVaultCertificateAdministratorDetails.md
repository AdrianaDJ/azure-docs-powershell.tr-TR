---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificateadministratordetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetails.md
ms.openlocfilehash: 6844a8f4858452a1ebf9df306d75e495603703aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935788"
---
# <span data-ttu-id="28292-101">New-AzKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="28292-101">New-AzKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="28292-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28292-102">SYNOPSIS</span></span>
<span data-ttu-id="28292-103">Bir bellek içi Sertifika Yöneticisi Ayrıntılar nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="28292-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="28292-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="28292-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28292-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="28292-105">DESCRIPTION</span></span>
<span data-ttu-id="28292-106">**New-Azanahtarvaultcertificatetındetails** cmdlet 'i, bellek içi Sertifika Yöneticisi Ayrıntılar nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="28292-106">The **New-AzKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="28292-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="28292-107">EXAMPLES</span></span>

### <span data-ttu-id="28292-108">Örnek 1: Sertifika Yöneticisi Ayrıntılar nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="28292-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="28292-109">Bu komut, bir bellek içi Sertifika Yöneticisi Ayrıntılar nesnesi oluşturur ve $AdminDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="28292-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="28292-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="28292-110">PARAMETERS</span></span>

### <span data-ttu-id="28292-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28292-111">-DefaultProfile</span></span>
<span data-ttu-id="28292-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="28292-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28292-113">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="28292-113">-EmailAddress</span></span>
<span data-ttu-id="28292-114">Sertifika yöneticisinin e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="28292-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="28292-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="28292-115">-FirstName</span></span>
<span data-ttu-id="28292-116">Sertifika yöneticisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="28292-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="28292-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="28292-117">-LastName</span></span>
<span data-ttu-id="28292-118">Sertifika yöneticisinin soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="28292-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="28292-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="28292-119">-PhoneNumber</span></span>
<span data-ttu-id="28292-120">Sertifika yöneticisinin telefon numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="28292-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="28292-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="28292-121">-Confirm</span></span>
<span data-ttu-id="28292-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="28292-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28292-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28292-123">-WhatIf</span></span>
<span data-ttu-id="28292-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="28292-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28292-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="28292-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28292-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28292-126">CommonParameters</span></span>
<span data-ttu-id="28292-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="28292-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28292-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28292-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28292-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="28292-129">INPUTS</span></span>

### <span data-ttu-id="28292-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="28292-130">None</span></span>
<span data-ttu-id="28292-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="28292-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="28292-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="28292-132">OUTPUTS</span></span>

### <span data-ttu-id="28292-133">Microsoft. Azure. Commands. Keykasa. modeller. Keyvaultcertificate\administrators ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="28292-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="28292-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="28292-134">NOTES</span></span>

## <span data-ttu-id="28292-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="28292-135">RELATED LINKS</span></span>

[<span data-ttu-id="28292-136">Yeni-Aztuş Vaultcertificateorganizationdetails</span><span class="sxs-lookup"><span data-stu-id="28292-136">New-AzKeyVaultCertificateOrganizationDetails</span></span>](./New-AzKeyVaultCertificateOrganizationDetails.md)

