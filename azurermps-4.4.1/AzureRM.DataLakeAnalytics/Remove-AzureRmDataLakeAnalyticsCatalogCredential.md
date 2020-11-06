---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: fc25b0a6605632da44d2b198c4bb30c515b2e456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587955"
---
# <span data-ttu-id="5528d-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="5528d-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="5528d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5528d-102">SYNOPSIS</span></span>
<span data-ttu-id="5528d-103">Azure Data Lake Analytics kimlik bilgisini siler.</span><span class="sxs-lookup"><span data-stu-id="5528d-103">Deletes an Azure Data Lake Analytics credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5528d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5528d-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5528d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5528d-105">DESCRIPTION</span></span>
<span data-ttu-id="5528d-106">Remove-AzureRmDataLakeAnalyticsCatalogCredential cmdlet 'i bir Azure Data Lake Analytics kataloğu kimlik bilgisini siler.</span><span class="sxs-lookup"><span data-stu-id="5528d-106">The Remove-AzureRmDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="5528d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5528d-107">EXAMPLES</span></span>

### <span data-ttu-id="5528d-108">Örnek 1: kimlik bilgisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="5528d-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="5528d-109">Bu komut, belirtilen Data Lake Analytics Katalog kimlik bilgisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5528d-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="5528d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5528d-110">PARAMETERS</span></span>

### <span data-ttu-id="5528d-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="5528d-111">-Account</span></span>
<span data-ttu-id="5528d-112">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5528d-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="5528d-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5528d-113">-DatabaseName</span></span>
<span data-ttu-id="5528d-114">Kimlik bilgilerini tutan veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5528d-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="5528d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5528d-115">-Force</span></span>
<span data-ttu-id="5528d-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="5528d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5528d-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="5528d-117">-Name</span></span>
<span data-ttu-id="5528d-118">Kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5528d-118">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="5528d-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5528d-119">-PassThru</span></span>
<span data-ttu-id="5528d-120">Bu cmdlet 'in işlemin tamamlanmasını beklemediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5528d-120">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="5528d-121">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="5528d-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5528d-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="5528d-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5528d-123">-Parola</span><span class="sxs-lookup"><span data-stu-id="5528d-123">-Password</span></span>
<span data-ttu-id="5528d-124">Kimlik bilgisinin parolası.</span><span class="sxs-lookup"><span data-stu-id="5528d-124">The password for the credential.</span></span>
<span data-ttu-id="5528d-125">Arayan hesabın sahibi değilse bu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5528d-125">This is required if the caller is not the owner of the account.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5528d-126">-Recurse</span><span class="sxs-lookup"><span data-stu-id="5528d-126">-Recurse</span></span>
<span data-ttu-id="5528d-127">Bu silme işleminin, bu kimlik bilgilerine bağımlı olan tüm kaynakları silip, sonra da silmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5528d-127">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5528d-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="5528d-128">-Confirm</span></span>
<span data-ttu-id="5528d-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5528d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5528d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5528d-130">-WhatIf</span></span>
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

### <span data-ttu-id="5528d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5528d-131">-DefaultProfile</span></span>
<span data-ttu-id="5528d-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5528d-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5528d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5528d-133">CommonParameters</span></span>
<span data-ttu-id="5528d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5528d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5528d-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5528d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5528d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5528d-136">INPUTS</span></span>

## <span data-ttu-id="5528d-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5528d-137">OUTPUTS</span></span>

### <span data-ttu-id="5528d-138">bool</span><span class="sxs-lookup"><span data-stu-id="5528d-138">bool</span></span>
<span data-ttu-id="5528d-139">Geçiş belirtildiyse, işlem tamamlandığında doğru değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5528d-139">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="5528d-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5528d-140">NOTES</span></span>

## <span data-ttu-id="5528d-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5528d-141">RELATED LINKS</span></span>

