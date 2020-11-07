---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 7F063C03-3EAA-4D90-BC4B-E29721B328D9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 16716b0df5867832d51ed00797f19d5dfc0f0b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763773"
---
# <span data-ttu-id="117ba-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="117ba-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="117ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="117ba-102">SYNOPSIS</span></span>
<span data-ttu-id="117ba-103">Veri Lake Analytics gizliliğini siler.</span><span class="sxs-lookup"><span data-stu-id="117ba-103">Deletes a Data Lake Analytics secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="117ba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="117ba-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [[-Name] <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="117ba-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="117ba-105">DESCRIPTION</span></span>
<span data-ttu-id="117ba-106">**Remove-Azurermdatalakeanalizleri Ticdağın**</span><span class="sxs-lookup"><span data-stu-id="117ba-106">The **Remove-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet deletes an Azure Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="117ba-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="117ba-107">EXAMPLES</span></span>

### <span data-ttu-id="117ba-108">Örnek 1: parolayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="117ba-108">Example 1: Remove a secret</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdla" -DatabaseName "DatabaseName" -Name "SecretName"
```

<span data-ttu-id="117ba-109">Bu komut, belirtilen Data Lake Analytics Katalog gizliliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="117ba-109">This command removes the specified Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="117ba-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="117ba-110">PARAMETERS</span></span>

### <span data-ttu-id="117ba-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="117ba-111">-Account</span></span>
<span data-ttu-id="117ba-112">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="117ba-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="117ba-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="117ba-113">-DatabaseName</span></span>
<span data-ttu-id="117ba-114">Parolayı içeren veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="117ba-114">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="117ba-115">-Force</span><span class="sxs-lookup"><span data-stu-id="117ba-115">-Force</span></span>
<span data-ttu-id="117ba-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="117ba-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="117ba-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="117ba-117">-Name</span></span>
<span data-ttu-id="117ba-118">Parolanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="117ba-118">Specifies the name of the secret.</span></span>

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

### <span data-ttu-id="117ba-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="117ba-119">-PassThru</span></span>
<span data-ttu-id="117ba-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="117ba-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="117ba-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="117ba-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="117ba-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="117ba-122">-Confirm</span></span>
<span data-ttu-id="117ba-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="117ba-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="117ba-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="117ba-124">-WhatIf</span></span>
<span data-ttu-id="117ba-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="117ba-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="117ba-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="117ba-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="117ba-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="117ba-127">-DefaultProfile</span></span>
<span data-ttu-id="117ba-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="117ba-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="117ba-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="117ba-129">CommonParameters</span></span>
<span data-ttu-id="117ba-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="117ba-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="117ba-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="117ba-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="117ba-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="117ba-132">INPUTS</span></span>

## <span data-ttu-id="117ba-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="117ba-133">OUTPUTS</span></span>

### <span data-ttu-id="117ba-134">bool</span><span class="sxs-lookup"><span data-stu-id="117ba-134">bool</span></span>
<span data-ttu-id="117ba-135">Geçiş belirtildiyse, işlem tamamlandığında doğru değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="117ba-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="117ba-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="117ba-136">NOTES</span></span>

## <span data-ttu-id="117ba-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="117ba-137">RELATED LINKS</span></span>

[<span data-ttu-id="117ba-138">Yeni-Azurermdatalakeanalyzer Tic, Alogsecret</span><span class="sxs-lookup"><span data-stu-id="117ba-138">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="117ba-139">Set-Azurermdatalakeanalyzer Tic, Alogsecret</span><span class="sxs-lookup"><span data-stu-id="117ba-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


