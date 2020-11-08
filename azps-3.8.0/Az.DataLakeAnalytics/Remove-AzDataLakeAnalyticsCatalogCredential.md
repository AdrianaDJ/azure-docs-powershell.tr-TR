---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 9fbc00fe190e0a53fc9c41a6894ec35a7f8d9129
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096308"
---
# <span data-ttu-id="56d21-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="56d21-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="56d21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56d21-102">SYNOPSIS</span></span>
<span data-ttu-id="56d21-103">Azure Data Lake Analytics kimlik bilgisini siler.</span><span class="sxs-lookup"><span data-stu-id="56d21-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="56d21-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56d21-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56d21-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="56d21-105">DESCRIPTION</span></span>
<span data-ttu-id="56d21-106">Remove-AzDataLakeAnalyticsCatalogCredential cmdlet 'i bir Azure Data Lake Analytics kataloğu kimlik bilgisini siler.</span><span class="sxs-lookup"><span data-stu-id="56d21-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="56d21-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56d21-107">EXAMPLES</span></span>

### <span data-ttu-id="56d21-108">Örnek 1: kimlik bilgisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="56d21-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="56d21-109">Bu komut, belirtilen Data Lake Analytics Katalog kimlik bilgisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="56d21-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="56d21-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56d21-110">PARAMETERS</span></span>

### <span data-ttu-id="56d21-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="56d21-111">-Account</span></span>
<span data-ttu-id="56d21-112">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="56d21-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="56d21-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="56d21-113">-DatabaseName</span></span>
<span data-ttu-id="56d21-114">Kimlik bilgilerini tutan veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="56d21-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="56d21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d21-115">-DefaultProfile</span></span>
<span data-ttu-id="56d21-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="56d21-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56d21-117">-Force</span><span class="sxs-lookup"><span data-stu-id="56d21-117">-Force</span></span>
<span data-ttu-id="56d21-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="56d21-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="56d21-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="56d21-119">-Name</span></span>
<span data-ttu-id="56d21-120">Kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="56d21-120">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="56d21-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="56d21-121">-PassThru</span></span>
<span data-ttu-id="56d21-122">Bu cmdlet 'in işlemin tamamlanmasını beklemediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="56d21-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="56d21-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="56d21-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="56d21-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="56d21-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="56d21-125">-Parola</span><span class="sxs-lookup"><span data-stu-id="56d21-125">-Password</span></span>
<span data-ttu-id="56d21-126">Kimlik bilgisinin parolası.</span><span class="sxs-lookup"><span data-stu-id="56d21-126">The password for the credential.</span></span>
<span data-ttu-id="56d21-127">Arayan hesabın sahibi değilse bu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="56d21-127">This is required if the caller is not the owner of the account.</span></span>

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

### <span data-ttu-id="56d21-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="56d21-128">-Recurse</span></span>
<span data-ttu-id="56d21-129">Bu silme işleminin, bu kimlik bilgilerine bağımlı olan tüm kaynakları silip, sonra da silmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="56d21-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="56d21-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="56d21-130">-Confirm</span></span>
<span data-ttu-id="56d21-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="56d21-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56d21-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56d21-132">-WhatIf</span></span>
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

### <span data-ttu-id="56d21-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d21-133">CommonParameters</span></span>
<span data-ttu-id="56d21-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56d21-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d21-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56d21-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d21-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56d21-136">INPUTS</span></span>

### <span data-ttu-id="56d21-137">System. String</span><span class="sxs-lookup"><span data-stu-id="56d21-137">System.String</span></span>

### <span data-ttu-id="56d21-138">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="56d21-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="56d21-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="56d21-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="56d21-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56d21-140">OUTPUTS</span></span>

### <span data-ttu-id="56d21-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="56d21-141">System.Boolean</span></span>

## <span data-ttu-id="56d21-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56d21-142">NOTES</span></span>

## <span data-ttu-id="56d21-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56d21-143">RELATED LINKS</span></span>
