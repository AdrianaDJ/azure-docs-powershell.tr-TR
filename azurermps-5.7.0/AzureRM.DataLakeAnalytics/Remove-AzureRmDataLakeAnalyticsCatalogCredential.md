---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: af6acce52ee41297e650abb76188324ecf313679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588947"
---
# <span data-ttu-id="8ca28-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="8ca28-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="8ca28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ca28-102">SYNOPSIS</span></span>
<span data-ttu-id="8ca28-103">Azure Data Lake Analytics kimlik bilgisini siler.</span><span class="sxs-lookup"><span data-stu-id="8ca28-103">Deletes an Azure Data Lake Analytics credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ca28-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ca28-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ca28-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ca28-105">DESCRIPTION</span></span>
<span data-ttu-id="8ca28-106">Remove-AzureRmDataLakeAnalyticsCatalogCredential cmdlet 'i bir Azure Data Lake Analytics kataloğu kimlik bilgisini siler.</span><span class="sxs-lookup"><span data-stu-id="8ca28-106">The Remove-AzureRmDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="8ca28-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ca28-107">EXAMPLES</span></span>

### <span data-ttu-id="8ca28-108">Örnek 1: kimlik bilgisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="8ca28-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="8ca28-109">Bu komut, belirtilen Data Lake Analytics Katalog kimlik bilgisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8ca28-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="8ca28-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ca28-110">PARAMETERS</span></span>

### <span data-ttu-id="8ca28-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="8ca28-111">-Account</span></span>
<span data-ttu-id="8ca28-112">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ca28-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="8ca28-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8ca28-113">-DatabaseName</span></span>
<span data-ttu-id="8ca28-114">Kimlik bilgilerini tutan veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ca28-114">Specifies the name of the database that holds the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ca28-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ca28-115">-DefaultProfile</span></span>
<span data-ttu-id="8ca28-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8ca28-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ca28-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8ca28-117">-Force</span></span>
<span data-ttu-id="8ca28-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="8ca28-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8ca28-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="8ca28-119">-Name</span></span>
<span data-ttu-id="8ca28-120">Kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ca28-120">Specifies the name of the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ca28-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8ca28-121">-PassThru</span></span>
<span data-ttu-id="8ca28-122">Bu cmdlet 'in işlemin tamamlanmasını beklemediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ca28-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="8ca28-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="8ca28-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8ca28-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="8ca28-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8ca28-125">-Parola</span><span class="sxs-lookup"><span data-stu-id="8ca28-125">-Password</span></span>
<span data-ttu-id="8ca28-126">Kimlik bilgisinin parolası.</span><span class="sxs-lookup"><span data-stu-id="8ca28-126">The password for the credential.</span></span>
<span data-ttu-id="8ca28-127">Arayan hesabın sahibi değilse bu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="8ca28-127">This is required if the caller is not the owner of the account.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ca28-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="8ca28-128">-Recurse</span></span>
<span data-ttu-id="8ca28-129">Bu silme işleminin, bu kimlik bilgilerine bağımlı olan tüm kaynakları silip, sonra da silmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ca28-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="8ca28-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="8ca28-130">-Confirm</span></span>
<span data-ttu-id="8ca28-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8ca28-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ca28-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ca28-132">-WhatIf</span></span>
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

### <span data-ttu-id="8ca28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ca28-133">CommonParameters</span></span>
<span data-ttu-id="8ca28-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ca28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ca28-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ca28-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ca28-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ca28-136">INPUTS</span></span>

### <span data-ttu-id="8ca28-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8ca28-137">None</span></span>
<span data-ttu-id="8ca28-138">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="8ca28-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8ca28-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ca28-139">OUTPUTS</span></span>

### <span data-ttu-id="8ca28-140">bool</span><span class="sxs-lookup"><span data-stu-id="8ca28-140">bool</span></span>
<span data-ttu-id="8ca28-141">Geçiş belirtildiyse, işlem tamamlandığında doğru değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8ca28-141">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="8ca28-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ca28-142">NOTES</span></span>

## <span data-ttu-id="8ca28-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ca28-143">RELATED LINKS</span></span>

