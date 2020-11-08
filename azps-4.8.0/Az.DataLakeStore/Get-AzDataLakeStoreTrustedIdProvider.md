---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: fb600edb4fd8d18ee82cb7f83d651e6588acaa42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107848"
---
# <span data-ttu-id="546b6-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="546b6-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="546b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="546b6-102">SYNOPSIS</span></span>
<span data-ttu-id="546b6-103">Belirtilen veri Lake Store 'da belirtilen güvenilen kimlik sağlayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="546b6-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="546b6-104">Sağlayıcı belirtilmezse, hesabın tüm sağlayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="546b6-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="546b6-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="546b6-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="546b6-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="546b6-106">DESCRIPTION</span></span>
<span data-ttu-id="546b6-107">**Get-AzDataLakeStoreTrustedIdProvider** cmdlet 'ı belirtilen veri Lake Store 'da belirtilen güvenilen kimlik sağlayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="546b6-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="546b6-108">Sağlayıcı belirtilmezse, hesabın tüm sağlayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="546b6-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="546b6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="546b6-109">EXAMPLES</span></span>

### <span data-ttu-id="546b6-110">Örnek 1: belirli bir güvenilen kimlik sağlayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="546b6-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="546b6-111">"ContosoADL" hesabından "MyProvider" adlı sağlayıcıyı döndürür</span><span class="sxs-lookup"><span data-stu-id="546b6-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="546b6-112">Örnek 2: bir hesaptaki tüm sağlayıcıları listeleme</span><span class="sxs-lookup"><span data-stu-id="546b6-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="546b6-113">"ContosoADL" hesabının altındaki tüm sağlayıcıları listeler</span><span class="sxs-lookup"><span data-stu-id="546b6-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="546b6-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="546b6-114">PARAMETERS</span></span>

### <span data-ttu-id="546b6-115">-Hesap</span><span class="sxs-lookup"><span data-stu-id="546b6-115">-Account</span></span>
<span data-ttu-id="546b6-116">, Güvenilir kimlik sağlayıcısını</span><span class="sxs-lookup"><span data-stu-id="546b6-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546b6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="546b6-117">-DefaultProfile</span></span>
<span data-ttu-id="546b6-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="546b6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="546b6-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="546b6-119">-Name</span></span>
<span data-ttu-id="546b6-120">Alınacak güvenilen kimlik sağlayıcısının adı</span><span class="sxs-lookup"><span data-stu-id="546b6-120">The name of the trusted identity provider to retrieve</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546b6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="546b6-121">-ResourceGroupName</span></span>
<span data-ttu-id="546b6-122">Belirtilen hesabın belirtilen güvenilen kimlik sağlayıcısını almak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="546b6-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546b6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="546b6-123">CommonParameters</span></span>
<span data-ttu-id="546b6-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="546b6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="546b6-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="546b6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="546b6-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="546b6-126">INPUTS</span></span>

### <span data-ttu-id="546b6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="546b6-127">System.String</span></span>

## <span data-ttu-id="546b6-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="546b6-128">OUTPUTS</span></span>

### <span data-ttu-id="546b6-129">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="546b6-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="546b6-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="546b6-130">NOTES</span></span>

## <span data-ttu-id="546b6-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="546b6-131">RELATED LINKS</span></span>
