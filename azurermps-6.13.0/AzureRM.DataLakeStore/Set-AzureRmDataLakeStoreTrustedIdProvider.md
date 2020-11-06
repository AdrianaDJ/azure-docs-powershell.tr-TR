---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 509c80f77d48cebd101703727cefb37399ed2577
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589571"
---
# <span data-ttu-id="75307-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="75307-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="75307-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75307-102">SYNOPSIS</span></span>
<span data-ttu-id="75307-103">Belirtilen veri Lake Store 'da belirtilen güvenilen kimlik sağlayıcısını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="75307-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75307-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75307-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75307-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="75307-105">DESCRIPTION</span></span>
<span data-ttu-id="75307-106">**Set-AzureRmDataLakeStoreTrustedIdProvider** cmdlet 'ı belirtilen veri Lake Store 'da belirtilen güvenilen kimlik sağlayıcısını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="75307-106">The **Set-AzureRmDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="75307-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75307-107">EXAMPLES</span></span>

### <span data-ttu-id="75307-108">Örnek 1: güvenilen kimlik sağlayıcısı uç noktasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="75307-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="75307-109">Bu, "ContosoADL" hesabındaki "" ContosoADL "güvenlik duvarı kuralı" https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="75307-109">This updates the provider endpoing for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="75307-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75307-110">PARAMETERS</span></span>

### <span data-ttu-id="75307-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="75307-111">-Account</span></span>
<span data-ttu-id="75307-112">Güvenilen kimlik sağlayıcısını ekleme</span><span class="sxs-lookup"><span data-stu-id="75307-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="75307-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75307-113">-DefaultProfile</span></span>
<span data-ttu-id="75307-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="75307-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75307-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="75307-115">-Name</span></span>
<span data-ttu-id="75307-116">Güvenilen kimlik sağlayıcısının adı.</span><span class="sxs-lookup"><span data-stu-id="75307-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="75307-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="75307-117">-ProviderEndpoint</span></span>
<span data-ttu-id="75307-118">Şu biçimdeki geçerli güvenilen sağlayıcı uç noktası: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="75307-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="75307-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75307-119">-ResourceGroupName</span></span>
<span data-ttu-id="75307-120">Güvenilen kimlik sağlayıcısını güncelleştirme hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75307-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="75307-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="75307-121">-Confirm</span></span>
<span data-ttu-id="75307-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="75307-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75307-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75307-123">-WhatIf</span></span>
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

### <span data-ttu-id="75307-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75307-124">CommonParameters</span></span>
<span data-ttu-id="75307-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75307-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75307-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75307-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75307-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75307-127">INPUTS</span></span>

### <span data-ttu-id="75307-128">System. String</span><span class="sxs-lookup"><span data-stu-id="75307-128">System.String</span></span>

## <span data-ttu-id="75307-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75307-129">OUTPUTS</span></span>

### <span data-ttu-id="75307-130">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="75307-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="75307-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75307-131">NOTES</span></span>

## <span data-ttu-id="75307-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75307-132">RELATED LINKS</span></span>
