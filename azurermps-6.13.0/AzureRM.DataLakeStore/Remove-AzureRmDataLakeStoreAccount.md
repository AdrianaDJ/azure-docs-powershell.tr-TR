---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 2e73878258a95cf0a7448ba8bfd578e83b69dce6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572809"
---
# <span data-ttu-id="edeea-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="edeea-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="edeea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edeea-102">SYNOPSIS</span></span>
<span data-ttu-id="edeea-103">Data Lake Store hesabını kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="edeea-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edeea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="edeea-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edeea-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="edeea-105">DESCRIPTION</span></span>
<span data-ttu-id="edeea-106">**Remove-AzureRmDataLakeStoreAccount** cmdlet 'ı bir Data Lake Store hesabını kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="edeea-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="edeea-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="edeea-107">EXAMPLES</span></span>

### <span data-ttu-id="edeea-108">Örnek 1: veri Lake Store hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="edeea-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="edeea-109">Bu komut, Data Lake Store 'dan ContosoADL adlı hesabı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="edeea-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="edeea-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="edeea-110">PARAMETERS</span></span>

### <span data-ttu-id="edeea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edeea-111">-DefaultProfile</span></span>
<span data-ttu-id="edeea-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="edeea-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edeea-113">-Force</span><span class="sxs-lookup"><span data-stu-id="edeea-113">-Force</span></span>
<span data-ttu-id="edeea-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="edeea-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="edeea-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="edeea-115">-Name</span></span>
<span data-ttu-id="edeea-116">Kaldırılacak hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="edeea-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="edeea-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="edeea-117">-PassThru</span></span>
<span data-ttu-id="edeea-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="edeea-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="edeea-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="edeea-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="edeea-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edeea-120">-ResourceGroupName</span></span>
<span data-ttu-id="edeea-121">Kaldırılacak hesabı içeren kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="edeea-121">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="edeea-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="edeea-122">-Confirm</span></span>
<span data-ttu-id="edeea-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="edeea-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edeea-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edeea-124">-WhatIf</span></span>
<span data-ttu-id="edeea-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="edeea-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edeea-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="edeea-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edeea-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edeea-127">CommonParameters</span></span>
<span data-ttu-id="edeea-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="edeea-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edeea-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edeea-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edeea-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="edeea-130">INPUTS</span></span>

### <span data-ttu-id="edeea-131">System. String</span><span class="sxs-lookup"><span data-stu-id="edeea-131">System.String</span></span>

## <span data-ttu-id="edeea-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="edeea-132">OUTPUTS</span></span>

### <span data-ttu-id="edeea-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="edeea-133">System.Boolean</span></span>

## <span data-ttu-id="edeea-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="edeea-134">NOTES</span></span>

## <span data-ttu-id="edeea-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="edeea-135">RELATED LINKS</span></span>

[<span data-ttu-id="edeea-136">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="edeea-136">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="edeea-137">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="edeea-137">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="edeea-138">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="edeea-138">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="edeea-139">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="edeea-139">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


