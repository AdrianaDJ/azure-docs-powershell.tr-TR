---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 204ee5a7a4d0e5247ae3de239dce650deb4cff0c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935780"
---
# <span data-ttu-id="8a8ba-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="8a8ba-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="8a8ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a8ba-102">SYNOPSIS</span></span>
<span data-ttu-id="8a8ba-103">Bir anahtar kasasından sertifika vereni siler.</span><span class="sxs-lookup"><span data-stu-id="8a8ba-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="8a8ba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a8ba-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a8ba-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a8ba-105">DESCRIPTION</span></span>
<span data-ttu-id="8a8ba-106">**Remove-Azkeyvaultcertificateıssuer** cmdlet 'i anahtar kasasından sertifika vereni siler.</span><span class="sxs-lookup"><span data-stu-id="8a8ba-106">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="8a8ba-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a8ba-107">EXAMPLES</span></span>

### <span data-ttu-id="8a8ba-108">Örnek 1: sertifika vereni kaldırma</span><span class="sxs-lookup"><span data-stu-id="8a8ba-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="8a8ba-109">Bu komut, TestIssuer01 adındaki sertifika veren 'i ContosoKV01 Key kasasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8a8ba-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="8a8ba-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a8ba-110">PARAMETERS</span></span>

### <span data-ttu-id="8a8ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a8ba-111">-DefaultProfile</span></span>
<span data-ttu-id="8a8ba-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8a8ba-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a8ba-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8a8ba-113">-Force</span></span>
<span data-ttu-id="8a8ba-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="8a8ba-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a8ba-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="8a8ba-115">-Name</span></span>
<span data-ttu-id="8a8ba-116">Kaldırılacak veren 'in adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a8ba-116">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a8ba-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8a8ba-117">-PassThru</span></span>
<span data-ttu-id="8a8ba-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="8a8ba-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8a8ba-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="8a8ba-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a8ba-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8a8ba-120">-VaultName</span></span>
<span data-ttu-id="8a8ba-121">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a8ba-121">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a8ba-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="8a8ba-122">-Confirm</span></span>
<span data-ttu-id="8a8ba-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8a8ba-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a8ba-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a8ba-124">-WhatIf</span></span>
<span data-ttu-id="8a8ba-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a8ba-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a8ba-126">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a8ba-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a8ba-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8a8ba-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a8ba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a8ba-128">CommonParameters</span></span>
<span data-ttu-id="8a8ba-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a8ba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a8ba-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a8ba-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a8ba-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a8ba-131">INPUTS</span></span>

### <span data-ttu-id="8a8ba-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8a8ba-132">None</span></span>
<span data-ttu-id="8a8ba-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="8a8ba-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a8ba-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a8ba-134">OUTPUTS</span></span>

### <span data-ttu-id="8a8ba-135">Microsoft. Azure. Commands. Keykasa. modeller. Keyvaultcertificateıssuer 'i</span><span class="sxs-lookup"><span data-stu-id="8a8ba-135">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="8a8ba-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a8ba-136">NOTES</span></span>

## <span data-ttu-id="8a8ba-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a8ba-137">RELATED LINKS</span></span>

[<span data-ttu-id="8a8ba-138">Get-Azanahtarvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="8a8ba-138">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="8a8ba-139">Set-Azanahtarvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="8a8ba-139">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


