---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: 4c732cdfc175c47e9bd8125234cb1d33f1b19097
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938835"
---
# <span data-ttu-id="5e1cd-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="5e1cd-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="5e1cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e1cd-102">SYNOPSIS</span></span>
<span data-ttu-id="5e1cd-103">Bir anahtar kasasından sertifika vereni siler.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e1cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e1cd-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e1cd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e1cd-105">DESCRIPTION</span></span>
<span data-ttu-id="5e1cd-106">**Remove-AzureKeyVaultCertificateIssuer** cmdlet 'i, bir anahtar kasasından sertifika vereni siler.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-106">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="5e1cd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e1cd-107">EXAMPLES</span></span>

### <span data-ttu-id="5e1cd-108">Örnek 1: sertifika vereni kaldırma</span><span class="sxs-lookup"><span data-stu-id="5e1cd-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="5e1cd-109">Bu komut, TestIssuer01 adındaki sertifika veren 'i ContosoKV01 Key kasasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="5e1cd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e1cd-110">PARAMETERS</span></span>

### <span data-ttu-id="5e1cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e1cd-111">-DefaultProfile</span></span>
<span data-ttu-id="5e1cd-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5e1cd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e1cd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5e1cd-113">-Force</span></span>
<span data-ttu-id="5e1cd-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5e1cd-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="5e1cd-115">-Name</span></span>
<span data-ttu-id="5e1cd-116">Kaldırılacak veren 'in adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-116">Specifies the name of the issuer to remove.</span></span>

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

### <span data-ttu-id="5e1cd-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5e1cd-117">-PassThru</span></span>
<span data-ttu-id="5e1cd-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5e1cd-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5e1cd-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5e1cd-120">-VaultName</span></span>
<span data-ttu-id="5e1cd-121">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="5e1cd-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="5e1cd-122">-Confirm</span></span>
<span data-ttu-id="5e1cd-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e1cd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e1cd-124">-WhatIf</span></span>
<span data-ttu-id="5e1cd-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e1cd-126">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e1cd-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e1cd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e1cd-128">CommonParameters</span></span>
<span data-ttu-id="5e1cd-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e1cd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e1cd-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e1cd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e1cd-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e1cd-131">INPUTS</span></span>

## <span data-ttu-id="5e1cd-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e1cd-132">OUTPUTS</span></span>

### <span data-ttu-id="5e1cd-133">Microsoft. Azure. Commands. Keykasa. modeller. Keyvaultcertificateıssuer 'i</span><span class="sxs-lookup"><span data-stu-id="5e1cd-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="5e1cd-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e1cd-134">NOTES</span></span>

## <span data-ttu-id="5e1cd-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e1cd-135">RELATED LINKS</span></span>

[<span data-ttu-id="5e1cd-136">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="5e1cd-136">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="5e1cd-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="5e1cd-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


