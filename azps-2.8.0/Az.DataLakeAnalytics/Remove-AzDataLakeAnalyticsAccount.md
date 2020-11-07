---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 5e62bc19ec400f3dbfff3c089880cd14ce95609e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752384"
---
# <span data-ttu-id="ddc30-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ddc30-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="ddc30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddc30-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc30-103">Data Lake Analytics hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="ddc30-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="ddc30-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ddc30-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddc30-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ddc30-105">DESCRIPTION</span></span>
<span data-ttu-id="ddc30-106">**Remove-Azdatalakeanalizticsaccount** cmdlet 'i kalıcı olarak bir Azure Data Lake Analytics hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="ddc30-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="ddc30-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ddc30-107">EXAMPLES</span></span>

### <span data-ttu-id="ddc30-108">Örnek 1: hesap kaldırma</span><span class="sxs-lookup"><span data-stu-id="ddc30-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="ddc30-109">Bu komut, belirtilen Data Lake Analytics hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ddc30-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="ddc30-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ddc30-110">PARAMETERS</span></span>

### <span data-ttu-id="ddc30-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc30-111">-DefaultProfile</span></span>
<span data-ttu-id="ddc30-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ddc30-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddc30-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ddc30-113">-Force</span></span>
<span data-ttu-id="ddc30-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ddc30-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ddc30-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ddc30-115">-Name</span></span>
<span data-ttu-id="ddc30-116">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddc30-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="ddc30-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ddc30-117">-PassThru</span></span>
<span data-ttu-id="ddc30-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="ddc30-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ddc30-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ddc30-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ddc30-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc30-120">-ResourceGroupName</span></span>
<span data-ttu-id="ddc30-121">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddc30-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="ddc30-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="ddc30-122">-Confirm</span></span>
<span data-ttu-id="ddc30-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ddc30-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddc30-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddc30-124">-WhatIf</span></span>
<span data-ttu-id="ddc30-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ddc30-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddc30-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ddc30-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddc30-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc30-127">CommonParameters</span></span>
<span data-ttu-id="ddc30-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ddc30-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc30-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddc30-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc30-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ddc30-130">INPUTS</span></span>

### <span data-ttu-id="ddc30-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ddc30-131">System.String</span></span>

## <span data-ttu-id="ddc30-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ddc30-132">OUTPUTS</span></span>

### <span data-ttu-id="ddc30-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ddc30-133">System.Boolean</span></span>

## <span data-ttu-id="ddc30-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ddc30-134">NOTES</span></span>

## <span data-ttu-id="ddc30-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ddc30-135">RELATED LINKS</span></span>

[<span data-ttu-id="ddc30-136">Get-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="ddc30-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ddc30-137">Yeni-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="ddc30-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ddc30-138">Set-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="ddc30-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ddc30-139">Test-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="ddc30-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


