---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 9bad5e162aaba3b1d1ffb0326a1b919420df18c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592629"
---
# <span data-ttu-id="3b34a-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3b34a-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="3b34a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b34a-102">SYNOPSIS</span></span>
<span data-ttu-id="3b34a-103">Data Lake Store hesabını kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="3b34a-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b34a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b34a-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b34a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b34a-105">DESCRIPTION</span></span>
<span data-ttu-id="3b34a-106">**Remove-AzureRmDataLakeStoreAccount** cmdlet 'ı bir Data Lake Store hesabını kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="3b34a-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="3b34a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b34a-107">EXAMPLES</span></span>

### <span data-ttu-id="3b34a-108">Örnek 1: veri Lake Store hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="3b34a-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="3b34a-109">Bu komut, Data Lake Store 'dan ContosoADL adlı hesabı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3b34a-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="3b34a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b34a-110">PARAMETERS</span></span>

### <span data-ttu-id="3b34a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3b34a-111">-Force</span></span>
<span data-ttu-id="3b34a-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3b34a-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3b34a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="3b34a-113">-Name</span></span>
<span data-ttu-id="3b34a-114">Kaldırılacak hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b34a-114">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="3b34a-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3b34a-115">-PassThru</span></span>
<span data-ttu-id="3b34a-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="3b34a-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3b34a-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="3b34a-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3b34a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b34a-118">-ResourceGroupName</span></span>
<span data-ttu-id="3b34a-119">Kaldırılacak hesabı içeren kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b34a-119">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="3b34a-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="3b34a-120">-Confirm</span></span>
<span data-ttu-id="3b34a-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3b34a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b34a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b34a-122">-WhatIf</span></span>
<span data-ttu-id="3b34a-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3b34a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b34a-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3b34a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b34a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b34a-125">-DefaultProfile</span></span>
<span data-ttu-id="3b34a-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b34a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b34a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b34a-127">CommonParameters</span></span>
<span data-ttu-id="3b34a-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b34a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b34a-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b34a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b34a-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b34a-130">INPUTS</span></span>

## <span data-ttu-id="3b34a-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b34a-131">OUTPUTS</span></span>

### <span data-ttu-id="3b34a-132">bool</span><span class="sxs-lookup"><span data-stu-id="3b34a-132">bool</span></span>
<span data-ttu-id="3b34a-133">Geçiş belirtildiyse, başarılı bir tamamlandığında doğru sonucunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="3b34a-133">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="3b34a-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b34a-134">NOTES</span></span>

## <span data-ttu-id="3b34a-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b34a-135">RELATED LINKS</span></span>

[<span data-ttu-id="3b34a-136">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3b34a-136">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="3b34a-137">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3b34a-137">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="3b34a-138">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3b34a-138">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="3b34a-139">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3b34a-139">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)

