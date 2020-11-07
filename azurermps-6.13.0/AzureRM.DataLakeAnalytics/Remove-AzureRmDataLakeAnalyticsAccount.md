---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: a04295bca6c664e583ae9653b1f3ed7d52aebf3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763865"
---
# <span data-ttu-id="f69f3-101">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f69f3-101">Remove-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="f69f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f69f3-102">SYNOPSIS</span></span>
<span data-ttu-id="f69f3-103">Data Lake Analytics hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="f69f3-103">Deletes a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f69f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f69f3-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f69f3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f69f3-105">DESCRIPTION</span></span>
<span data-ttu-id="f69f3-106">**Remove-Azurermdatalakeanalizizsaccount** cmdlet 'i, bir Azure Data Lake Analytics hesabını kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="f69f3-106">The **Remove-AzureRmDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f69f3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f69f3-107">EXAMPLES</span></span>

### <span data-ttu-id="f69f3-108">Örnek 1: hesap kaldırma</span><span class="sxs-lookup"><span data-stu-id="f69f3-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="f69f3-109">Bu komut, belirtilen Data Lake Analytics hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f69f3-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="f69f3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f69f3-110">PARAMETERS</span></span>

### <span data-ttu-id="f69f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f69f3-111">-DefaultProfile</span></span>
<span data-ttu-id="f69f3-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f69f3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f69f3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f69f3-113">-Force</span></span>
<span data-ttu-id="f69f3-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f69f3-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f69f3-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="f69f3-115">-Name</span></span>
<span data-ttu-id="f69f3-116">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f69f3-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="f69f3-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f69f3-117">-PassThru</span></span>
<span data-ttu-id="f69f3-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="f69f3-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f69f3-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="f69f3-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f69f3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f69f3-120">-ResourceGroupName</span></span>
<span data-ttu-id="f69f3-121">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f69f3-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="f69f3-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="f69f3-122">-Confirm</span></span>
<span data-ttu-id="f69f3-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f69f3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f69f3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f69f3-124">-WhatIf</span></span>
<span data-ttu-id="f69f3-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f69f3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f69f3-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f69f3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f69f3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f69f3-127">CommonParameters</span></span>
<span data-ttu-id="f69f3-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f69f3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f69f3-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f69f3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f69f3-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f69f3-130">INPUTS</span></span>

### <span data-ttu-id="f69f3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f69f3-131">System.String</span></span>

## <span data-ttu-id="f69f3-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f69f3-132">OUTPUTS</span></span>

### <span data-ttu-id="f69f3-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f69f3-133">System.Boolean</span></span>

## <span data-ttu-id="f69f3-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f69f3-134">NOTES</span></span>

## <span data-ttu-id="f69f3-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f69f3-135">RELATED LINKS</span></span>

[<span data-ttu-id="f69f3-136">Get-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="f69f3-136">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f69f3-137">Yeni-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="f69f3-137">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f69f3-138">Set-Azurermdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="f69f3-138">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f69f3-139">Test-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="f69f3-139">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


