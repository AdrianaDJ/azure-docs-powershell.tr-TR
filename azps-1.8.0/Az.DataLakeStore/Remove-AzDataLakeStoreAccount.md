---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
ms.openlocfilehash: edd03d0a5836393c20b9af2da1cd89502bd2030b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761060"
---
# <span data-ttu-id="56dde-101">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="56dde-101">Remove-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="56dde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56dde-102">SYNOPSIS</span></span>
<span data-ttu-id="56dde-103">Data Lake Store hesabını kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="56dde-103">Deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="56dde-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56dde-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56dde-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="56dde-105">DESCRIPTION</span></span>
<span data-ttu-id="56dde-106">**Remove-AzDataLakeStoreAccount** cmdlet 'ı bir Data Lake Store hesabını kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="56dde-106">The **Remove-AzDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="56dde-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56dde-107">EXAMPLES</span></span>

### <span data-ttu-id="56dde-108">Örnek 1: veri Lake Store hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="56dde-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="56dde-109">Bu komut, Data Lake Store 'dan ContosoADL adlı hesabı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="56dde-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="56dde-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56dde-110">PARAMETERS</span></span>

### <span data-ttu-id="56dde-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56dde-111">-DefaultProfile</span></span>
<span data-ttu-id="56dde-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="56dde-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56dde-113">-Force</span><span class="sxs-lookup"><span data-stu-id="56dde-113">-Force</span></span>
<span data-ttu-id="56dde-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="56dde-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="56dde-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="56dde-115">-Name</span></span>
<span data-ttu-id="56dde-116">Kaldırılacak hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="56dde-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="56dde-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="56dde-117">-PassThru</span></span>
<span data-ttu-id="56dde-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="56dde-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="56dde-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="56dde-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="56dde-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56dde-120">-ResourceGroupName</span></span>
<span data-ttu-id="56dde-121">Kaldırılacak hesabı içeren kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="56dde-121">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="56dde-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="56dde-122">-Confirm</span></span>
<span data-ttu-id="56dde-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="56dde-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56dde-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56dde-124">-WhatIf</span></span>
<span data-ttu-id="56dde-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="56dde-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56dde-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="56dde-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56dde-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56dde-127">CommonParameters</span></span>
<span data-ttu-id="56dde-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56dde-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56dde-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56dde-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56dde-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56dde-130">INPUTS</span></span>

### <span data-ttu-id="56dde-131">System. String</span><span class="sxs-lookup"><span data-stu-id="56dde-131">System.String</span></span>

## <span data-ttu-id="56dde-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56dde-132">OUTPUTS</span></span>

### <span data-ttu-id="56dde-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="56dde-133">System.Boolean</span></span>

## <span data-ttu-id="56dde-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56dde-134">NOTES</span></span>

## <span data-ttu-id="56dde-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56dde-135">RELATED LINKS</span></span>

[<span data-ttu-id="56dde-136">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="56dde-136">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="56dde-137">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="56dde-137">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="56dde-138">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="56dde-138">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="56dde-139">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="56dde-139">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)

