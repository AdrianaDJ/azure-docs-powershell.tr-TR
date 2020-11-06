---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c769e3e084f0ac5fd6df22bae81a4d8df99dc700
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594489"
---
# <span data-ttu-id="0febd-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="0febd-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="0febd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0febd-102">SYNOPSIS</span></span>
<span data-ttu-id="0febd-103">Belirtilen veri Lake Store 'da belirtilen güvenilen kimlik sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0febd-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0febd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0febd-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0febd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0febd-105">DESCRIPTION</span></span>
<span data-ttu-id="0febd-106">**Remove-AzureRmDataLakeStoreTrustedIdProvider** cmdlet 'ı belirtilen Data Lake Store 'da belirtilen güvenilen kimlik sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0febd-106">The **Remove-AzureRmDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="0febd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0febd-107">EXAMPLES</span></span>

### <span data-ttu-id="0febd-108">Örnek 1: güvenilir bir kimlik sağlayıcısını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="0febd-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="0febd-109">"Benimsağlayıcı" sağlayıcısını "ContosoADL" hesabından kaldırır</span><span class="sxs-lookup"><span data-stu-id="0febd-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="0febd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0febd-110">PARAMETERS</span></span>

### <span data-ttu-id="0febd-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="0febd-111">-Account</span></span>
<span data-ttu-id="0febd-112">Güvenilir kimlik sağlayıcısını kaldırmak için Data Lake Store hesabı</span><span class="sxs-lookup"><span data-stu-id="0febd-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0febd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0febd-113">-DefaultProfile</span></span>
<span data-ttu-id="0febd-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0febd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0febd-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="0febd-115">-Name</span></span>
<span data-ttu-id="0febd-116">Güvenilen kimlik sağlayıcısının adı.</span><span class="sxs-lookup"><span data-stu-id="0febd-116">The name of the trusted identity provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0febd-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0febd-117">-PassThru</span></span>
<span data-ttu-id="0febd-118">Silme işleminin sonucunu belirten bir Boole yanıtının döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0febd-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0febd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0febd-119">-ResourceGroupName</span></span>
<span data-ttu-id="0febd-120">Güvenilen kimlik sağlayıcısını kaldırmak istediğiniz hesabı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0febd-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0febd-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="0febd-121">-Confirm</span></span>
<span data-ttu-id="0febd-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0febd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0febd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0febd-123">-WhatIf</span></span>
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

### <span data-ttu-id="0febd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0febd-124">CommonParameters</span></span>
<span data-ttu-id="0febd-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0febd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0febd-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0febd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0febd-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0febd-127">INPUTS</span></span>

### <span data-ttu-id="0febd-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0febd-128">None</span></span>
<span data-ttu-id="0febd-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0febd-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0febd-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0febd-130">OUTPUTS</span></span>

### <span data-ttu-id="0febd-131">bool</span><span class="sxs-lookup"><span data-stu-id="0febd-131">bool</span></span>
<span data-ttu-id="0febd-132">Geçiş belirtildiyse, başarılı bir tamamlandığında doğru sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="0febd-132">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="0febd-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0febd-133">NOTES</span></span>

## <span data-ttu-id="0febd-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0febd-134">RELATED LINKS</span></span>

