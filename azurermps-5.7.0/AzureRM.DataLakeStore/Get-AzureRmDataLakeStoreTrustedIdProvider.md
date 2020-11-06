---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c387ebb089ab7f9dfddaee818f26596f34ed91e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594088"
---
# <span data-ttu-id="6ef0d-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="6ef0d-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="6ef0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ef0d-102">SYNOPSIS</span></span>
<span data-ttu-id="6ef0d-103">Belirtilen veri Lake Store 'da belirtilen güvenilen kimlik sağlayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="6ef0d-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="6ef0d-104">Sağlayıcı belirtilmezse, hesabın tüm sağlayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="6ef0d-104">If no provider is specified, then lists all providers for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ef0d-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ef0d-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ef0d-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ef0d-106">DESCRIPTION</span></span>
<span data-ttu-id="6ef0d-107">**Get-AzureRmDataLakeStoreTrustedIdProvider** cmdlet 'ı belirtilen veri Lake Store 'da belirtilen güvenilen kimlik sağlayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="6ef0d-107">The **Get-AzureRmDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="6ef0d-108">Sağlayıcı belirtilmezse, hesabın tüm sağlayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="6ef0d-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="6ef0d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ef0d-109">EXAMPLES</span></span>

### <span data-ttu-id="6ef0d-110">Örnek 1: belirli bir güvenilen kimlik sağlayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="6ef0d-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="6ef0d-111">"ContosoADL" hesabından "MyProvider" adlı sağlayıcıyı döndürür</span><span class="sxs-lookup"><span data-stu-id="6ef0d-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="6ef0d-112">Örnek 2: bir hesaptaki tüm sağlayıcıları listeleme</span><span class="sxs-lookup"><span data-stu-id="6ef0d-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="6ef0d-113">"ContosoADL" hesabının altındaki tüm sağlayıcıları listeler</span><span class="sxs-lookup"><span data-stu-id="6ef0d-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="6ef0d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ef0d-114">PARAMETERS</span></span>

### <span data-ttu-id="6ef0d-115">-Hesap</span><span class="sxs-lookup"><span data-stu-id="6ef0d-115">-Account</span></span>
<span data-ttu-id="6ef0d-116">, Güvenilir kimlik sağlayıcısını</span><span class="sxs-lookup"><span data-stu-id="6ef0d-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="6ef0d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ef0d-117">-DefaultProfile</span></span>
<span data-ttu-id="6ef0d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6ef0d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ef0d-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="6ef0d-119">-Name</span></span>
<span data-ttu-id="6ef0d-120">Alınacak güvenilen kimlik sağlayıcısının adı</span><span class="sxs-lookup"><span data-stu-id="6ef0d-120">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="6ef0d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ef0d-121">-ResourceGroupName</span></span>
<span data-ttu-id="6ef0d-122">Belirtilen hesabın belirtilen güvenilen kimlik sağlayıcısını almak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6ef0d-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ef0d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ef0d-123">CommonParameters</span></span>
<span data-ttu-id="6ef0d-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ef0d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ef0d-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ef0d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ef0d-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ef0d-126">INPUTS</span></span>

### <span data-ttu-id="6ef0d-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6ef0d-127">None</span></span>
<span data-ttu-id="6ef0d-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6ef0d-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6ef0d-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ef0d-129">OUTPUTS</span></span>

### <span data-ttu-id="6ef0d-130">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="6ef0d-130">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="6ef0d-131">Belirtilen güvenilen kimlik sağlayıcısının ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="6ef0d-131">The details of the specified trusted identity provider.</span></span>

### <span data-ttu-id="6ef0d-132">'Te<DataLakeStoreTrustedIdProvider></span><span class="sxs-lookup"><span data-stu-id="6ef0d-132">IList<DataLakeStoreTrustedIdProvider></span></span>
<span data-ttu-id="6ef0d-133">Belirtilen hesaptaki güvenilen kimlik sağlayıcılarının listesi.</span><span class="sxs-lookup"><span data-stu-id="6ef0d-133">The list of trusted identity providers in the specified account.</span></span>

## <span data-ttu-id="6ef0d-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ef0d-134">NOTES</span></span>

## <span data-ttu-id="6ef0d-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ef0d-135">RELATED LINKS</span></span>

