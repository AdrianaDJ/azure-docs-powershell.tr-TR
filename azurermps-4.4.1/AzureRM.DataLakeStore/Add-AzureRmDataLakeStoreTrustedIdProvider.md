---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: f71fefdce069f1786125f8c65ba94d66fb67fa56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587945"
---
# <span data-ttu-id="4d40f-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="4d40f-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="4d40f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d40f-102">SYNOPSIS</span></span>
<span data-ttu-id="4d40f-103">Belirtilen Data Lake Store hesabına güvenilir bir kimlik sağlayıcısı ekler.</span><span class="sxs-lookup"><span data-stu-id="4d40f-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d40f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d40f-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d40f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d40f-105">DESCRIPTION</span></span>
<span data-ttu-id="4d40f-106">**Add-AzureRmDataLakeStoreTrustedIdProvider** cmdlet 'ı belirtilen Data Lake Store hesabına güvenilir bir kimlik sağlayıcısı ekler.</span><span class="sxs-lookup"><span data-stu-id="4d40f-106">The **Add-AzureRmDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="4d40f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d40f-107">EXAMPLES</span></span>

### <span data-ttu-id="4d40f-108">Örnek 1: güvenilir bir kimlik sağlayıcısı ekleme</span><span class="sxs-lookup"><span data-stu-id="4d40f-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="4d40f-109">"Benimsağlayıcı" sağlayıcısını sağlayıcı uç noktası "ContosoADL" hesabına ekler " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="4d40f-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="4d40f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d40f-110">PARAMETERS</span></span>

### <span data-ttu-id="4d40f-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="4d40f-111">-Account</span></span>
<span data-ttu-id="4d40f-112">Belirtilen güvenilen kimlik sağlayıcısını eklemek için Data Lake Store hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="4d40f-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="4d40f-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="4d40f-113">-Name</span></span>
<span data-ttu-id="4d40f-114">Eklenecek güvenilen kimlik sağlayıcısının adı</span><span class="sxs-lookup"><span data-stu-id="4d40f-114">The name of the trusted identity provider to add</span></span>

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

### <span data-ttu-id="4d40f-115">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d40f-115">-ProviderEndpoint</span></span>
<span data-ttu-id="4d40f-116">Şu biçimdeki geçerli güvenilen sağlayıcı uç noktası: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="4d40f-116">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d40f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d40f-117">-ResourceGroupName</span></span>
<span data-ttu-id="4d40f-118">Güvenilen kimlik sağlayıcısının ekleneceği hesabın bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4d40f-118">Name of resource group under which the account to add the trusted identity provider is.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d40f-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="4d40f-119">-Confirm</span></span>
<span data-ttu-id="4d40f-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4d40f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d40f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d40f-121">-WhatIf</span></span>
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

### <span data-ttu-id="4d40f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d40f-122">-DefaultProfile</span></span>
<span data-ttu-id="4d40f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4d40f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d40f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d40f-124">CommonParameters</span></span>
<span data-ttu-id="4d40f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d40f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d40f-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d40f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d40f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d40f-127">INPUTS</span></span>

## <span data-ttu-id="4d40f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d40f-128">OUTPUTS</span></span>

### <span data-ttu-id="4d40f-129">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="4d40f-129">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="4d40f-130">Ek güvenilen kimlik sağlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="4d40f-130">The added Trusted Identity Provider.</span></span>

## <span data-ttu-id="4d40f-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d40f-131">NOTES</span></span>

## <span data-ttu-id="4d40f-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d40f-132">RELATED LINKS</span></span>

