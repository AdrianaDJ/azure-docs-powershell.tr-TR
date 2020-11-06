---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 3ef23bcbddc1f8a5c5c235c72dac32f535a71a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593559"
---
# <span data-ttu-id="2243c-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2243c-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="2243c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2243c-102">SYNOPSIS</span></span>
<span data-ttu-id="2243c-103">Bir anahtar kasasından sertifika vereni siler.</span><span class="sxs-lookup"><span data-stu-id="2243c-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2243c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2243c-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2243c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2243c-105">DESCRIPTION</span></span>
<span data-ttu-id="2243c-106">**Remove-AzureKeyVaultCertificateIssuer** cmdlet 'i, bir anahtar kasasından sertifika vereni siler.</span><span class="sxs-lookup"><span data-stu-id="2243c-106">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="2243c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2243c-107">EXAMPLES</span></span>

### <span data-ttu-id="2243c-108">Örnek 1: sertifika vereni kaldırma</span><span class="sxs-lookup"><span data-stu-id="2243c-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="2243c-109">Bu komut, TestIssuer01 adındaki sertifika veren 'i ContosoKV01 Key kasasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2243c-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="2243c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2243c-110">PARAMETERS</span></span>

### <span data-ttu-id="2243c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2243c-111">-Force</span></span>
<span data-ttu-id="2243c-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="2243c-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2243c-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="2243c-113">-Name</span></span>
<span data-ttu-id="2243c-114">Kaldırılacak veren 'in adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2243c-114">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2243c-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2243c-115">-PassThru</span></span>
<span data-ttu-id="2243c-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="2243c-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2243c-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="2243c-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2243c-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2243c-118">-VaultName</span></span>
<span data-ttu-id="2243c-119">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2243c-119">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2243c-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="2243c-120">-Confirm</span></span>
<span data-ttu-id="2243c-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2243c-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2243c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2243c-122">-WhatIf</span></span>
<span data-ttu-id="2243c-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2243c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2243c-124">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2243c-124">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2243c-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2243c-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2243c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2243c-126">-DefaultProfile</span></span>
<span data-ttu-id="2243c-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2243c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2243c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2243c-128">CommonParameters</span></span>
<span data-ttu-id="2243c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2243c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2243c-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2243c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2243c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2243c-131">INPUTS</span></span>

## <span data-ttu-id="2243c-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2243c-132">OUTPUTS</span></span>

### <span data-ttu-id="2243c-133">Microsoft. Azure. Commands. Keykasa. modeller. Keyvaultcertificateıssuer 'i</span><span class="sxs-lookup"><span data-stu-id="2243c-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="2243c-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2243c-134">NOTES</span></span>

## <span data-ttu-id="2243c-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2243c-135">RELATED LINKS</span></span>

[<span data-ttu-id="2243c-136">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2243c-136">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="2243c-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2243c-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


