---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 23f1ba9185b2a33c910afb0fc7ff0deb2a1cbf5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587954"
---
# <span data-ttu-id="abf23-101">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="abf23-101">Remove-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="abf23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abf23-102">SYNOPSIS</span></span>
<span data-ttu-id="abf23-103">Data Lake Analytics hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="abf23-103">Deletes a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abf23-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="abf23-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abf23-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="abf23-105">DESCRIPTION</span></span>
<span data-ttu-id="abf23-106">**Remove-Azurermdatalakeanalizizsaccount** cmdlet 'i, bir Azure Data Lake Analytics hesabını kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="abf23-106">The **Remove-AzureRmDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="abf23-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="abf23-107">EXAMPLES</span></span>

### <span data-ttu-id="abf23-108">Örnek 1: hesap kaldırma</span><span class="sxs-lookup"><span data-stu-id="abf23-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="abf23-109">Bu komut, belirtilen Data Lake Analytics hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="abf23-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="abf23-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="abf23-110">PARAMETERS</span></span>

### <span data-ttu-id="abf23-111">-Force</span><span class="sxs-lookup"><span data-stu-id="abf23-111">-Force</span></span>
<span data-ttu-id="abf23-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="abf23-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf23-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="abf23-113">-Name</span></span>
<span data-ttu-id="abf23-114">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="abf23-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf23-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="abf23-115">-PassThru</span></span>
<span data-ttu-id="abf23-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="abf23-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="abf23-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="abf23-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="abf23-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf23-118">-ResourceGroupName</span></span>
<span data-ttu-id="abf23-119">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="abf23-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="abf23-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="abf23-120">-Confirm</span></span>
<span data-ttu-id="abf23-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="abf23-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abf23-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abf23-122">-WhatIf</span></span>
<span data-ttu-id="abf23-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="abf23-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abf23-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="abf23-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abf23-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf23-125">-DefaultProfile</span></span>
<span data-ttu-id="abf23-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="abf23-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abf23-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf23-127">CommonParameters</span></span>
<span data-ttu-id="abf23-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="abf23-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf23-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf23-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf23-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="abf23-130">INPUTS</span></span>

## <span data-ttu-id="abf23-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="abf23-131">OUTPUTS</span></span>

### <span data-ttu-id="abf23-132">bool</span><span class="sxs-lookup"><span data-stu-id="abf23-132">bool</span></span>
<span data-ttu-id="abf23-133">Geçiş belirtildiyse, işlem tamamlandığında doğru değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="abf23-133">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="abf23-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="abf23-134">NOTES</span></span>

## <span data-ttu-id="abf23-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="abf23-135">RELATED LINKS</span></span>

[<span data-ttu-id="abf23-136">Get-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="abf23-136">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="abf23-137">Yeni-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="abf23-137">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="abf23-138">Set-Azurermdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="abf23-138">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="abf23-139">Test-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="abf23-139">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


