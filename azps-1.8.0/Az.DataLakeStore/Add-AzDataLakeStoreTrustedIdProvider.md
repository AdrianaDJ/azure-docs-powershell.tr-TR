---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: dc315e2ee69fbccd12ed1f07057e51dab30c04e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916916"
---
# <span data-ttu-id="531c8-101">Add-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="531c8-101">Add-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="531c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="531c8-102">SYNOPSIS</span></span>
<span data-ttu-id="531c8-103">Belirtilen Data Lake Store hesabına güvenilir bir kimlik sağlayıcısı ekler.</span><span class="sxs-lookup"><span data-stu-id="531c8-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="531c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="531c8-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="531c8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="531c8-105">DESCRIPTION</span></span>
<span data-ttu-id="531c8-106">**Add-AzDataLakeStoreTrustedIdProvider** cmdlet 'ı belirtilen Data Lake Store hesabına güvenilir bir kimlik sağlayıcısı ekler.</span><span class="sxs-lookup"><span data-stu-id="531c8-106">The **Add-AzDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="531c8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="531c8-107">EXAMPLES</span></span>

### <span data-ttu-id="531c8-108">Örnek 1: güvenilir bir kimlik sağlayıcısı ekleme</span><span class="sxs-lookup"><span data-stu-id="531c8-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="531c8-109">"Benimsağlayıcı" sağlayıcısını sağlayıcı uç noktası "ContosoADL" hesabına ekler " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="531c8-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="531c8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="531c8-110">PARAMETERS</span></span>

### <span data-ttu-id="531c8-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="531c8-111">-Account</span></span>
<span data-ttu-id="531c8-112">Belirtilen güvenilen kimlik sağlayıcısını eklemek için Data Lake Store hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="531c8-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="531c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="531c8-113">-DefaultProfile</span></span>
<span data-ttu-id="531c8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="531c8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="531c8-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="531c8-115">-Name</span></span>
<span data-ttu-id="531c8-116">Eklenecek güvenilen kimlik sağlayıcısının adı</span><span class="sxs-lookup"><span data-stu-id="531c8-116">The name of the trusted identity provider to add</span></span>

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

### <span data-ttu-id="531c8-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="531c8-117">-ProviderEndpoint</span></span>
<span data-ttu-id="531c8-118">Geçerli güvenilen sağlayıcı uç noktası: https://sts.windows.net/\<provider identity \> "</span><span class="sxs-lookup"><span data-stu-id="531c8-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

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

### <span data-ttu-id="531c8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="531c8-119">-ResourceGroupName</span></span>
<span data-ttu-id="531c8-120">Güvenilen kimlik sağlayıcısının ekleneceği hesabın bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="531c8-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

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

### <span data-ttu-id="531c8-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="531c8-121">-Confirm</span></span>
<span data-ttu-id="531c8-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="531c8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="531c8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="531c8-123">-WhatIf</span></span>
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

### <span data-ttu-id="531c8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="531c8-124">CommonParameters</span></span>
<span data-ttu-id="531c8-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="531c8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="531c8-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="531c8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="531c8-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="531c8-127">INPUTS</span></span>

### <span data-ttu-id="531c8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="531c8-128">System.String</span></span>

## <span data-ttu-id="531c8-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="531c8-129">OUTPUTS</span></span>

### <span data-ttu-id="531c8-130">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="531c8-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="531c8-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="531c8-131">NOTES</span></span>

## <span data-ttu-id="531c8-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="531c8-132">RELATED LINKS</span></span>
