---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateadministratordetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
ms.openlocfilehash: 01d0718e4efeae093b7bd9ed4fc2c6bca4cf7f62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764997"
---
# <span data-ttu-id="9ecb1-101">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="9ecb1-101">New-AzureKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="9ecb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ecb1-102">SYNOPSIS</span></span>
<span data-ttu-id="9ecb1-103">Bir bellek içi Sertifika Yöneticisi Ayrıntılar nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ecb1-103">Creates an in-memory certificate administrator details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ecb1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ecb1-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ecb1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ecb1-105">DESCRIPTION</span></span>
<span data-ttu-id="9ecb1-106">**New-AzureKeyVaultCertificateAdministratorDetails** cmdlet 'i, bellek içi Sertifika Yöneticisi Ayrıntılar nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ecb1-106">The **New-AzureKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="9ecb1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ecb1-107">EXAMPLES</span></span>

### <span data-ttu-id="9ecb1-108">Örnek 1: Sertifika Yöneticisi Ayrıntılar nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9ecb1-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="9ecb1-109">Bu komut, bir bellek içi Sertifika Yöneticisi Ayrıntılar nesnesi oluşturur ve $AdminDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9ecb1-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="9ecb1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ecb1-110">PARAMETERS</span></span>

### <span data-ttu-id="9ecb1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ecb1-111">-DefaultProfile</span></span>
<span data-ttu-id="9ecb1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9ecb1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ecb1-113">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="9ecb1-113">-EmailAddress</span></span>
<span data-ttu-id="9ecb1-114">Sertifika yöneticisinin e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ecb1-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="9ecb1-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="9ecb1-115">-FirstName</span></span>
<span data-ttu-id="9ecb1-116">Sertifika yöneticisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ecb1-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="9ecb1-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="9ecb1-117">-LastName</span></span>
<span data-ttu-id="9ecb1-118">Sertifika yöneticisinin soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ecb1-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="9ecb1-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="9ecb1-119">-PhoneNumber</span></span>
<span data-ttu-id="9ecb1-120">Sertifika yöneticisinin telefon numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ecb1-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="9ecb1-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="9ecb1-121">-Confirm</span></span>
<span data-ttu-id="9ecb1-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9ecb1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ecb1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ecb1-123">-WhatIf</span></span>
<span data-ttu-id="9ecb1-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9ecb1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ecb1-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9ecb1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ecb1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ecb1-126">CommonParameters</span></span>
<span data-ttu-id="9ecb1-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ecb1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ecb1-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ecb1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ecb1-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ecb1-129">INPUTS</span></span>

### <span data-ttu-id="9ecb1-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9ecb1-130">None</span></span>
<span data-ttu-id="9ecb1-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="9ecb1-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9ecb1-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ecb1-132">OUTPUTS</span></span>

### <span data-ttu-id="9ecb1-133">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificate\administrators ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="9ecb1-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="9ecb1-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ecb1-134">NOTES</span></span>

## <span data-ttu-id="9ecb1-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ecb1-135">RELATED LINKS</span></span>

[<span data-ttu-id="9ecb1-136">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="9ecb1-136">New-AzureKeyVaultCertificateOrganizationDetails</span></span>](./New-AzureKeyVaultCertificateOrganizationDetails.md)

