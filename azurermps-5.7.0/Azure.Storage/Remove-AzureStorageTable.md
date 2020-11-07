---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
ms.openlocfilehash: 7423cbb6995430523beb137ef10eb6f1a53c959c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763069"
---
# <span data-ttu-id="f8d37-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="f8d37-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="f8d37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8d37-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d37-103">Depolama tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f8d37-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8d37-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8d37-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8d37-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8d37-105">DESCRIPTION</span></span>
<span data-ttu-id="f8d37-106">**Remove-AzureStorageTable** cmdlet 'ı, Azure 'daki depolama hesabından bir veya daha fazla depolama tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f8d37-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="f8d37-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8d37-107">EXAMPLES</span></span>

### <span data-ttu-id="f8d37-108">Örnek 1: tablo kaldırma</span><span class="sxs-lookup"><span data-stu-id="f8d37-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="f8d37-109">Bu komut tabloyu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f8d37-109">This command removes a table.</span></span>

### <span data-ttu-id="f8d37-110">Örnek 2: birkaç tabloyu kaldırma</span><span class="sxs-lookup"><span data-stu-id="f8d37-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="f8d37-111">Bu örnekte, desen tablosuyla eşleşen tüm tabloları almak için *Name* parametresiyle birlikte joker karakter kullanılır ve ardından tabloları kaldırmak için sonucu ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="f8d37-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="f8d37-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8d37-112">PARAMETERS</span></span>

### <span data-ttu-id="f8d37-113">-Context</span><span class="sxs-lookup"><span data-stu-id="f8d37-113">-Context</span></span>
<span data-ttu-id="f8d37-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8d37-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="f8d37-115">Bunu, New-AzureStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f8d37-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d37-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f8d37-116">-Force</span></span>
<span data-ttu-id="f8d37-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f8d37-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f8d37-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="f8d37-118">-Name</span></span>
<span data-ttu-id="f8d37-119">Kaldırılacak tablonun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8d37-119">Specifies the name of the table to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d37-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f8d37-120">-PassThru</span></span>
<span data-ttu-id="f8d37-121">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="f8d37-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="f8d37-122">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="f8d37-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f8d37-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="f8d37-123">-Confirm</span></span>
<span data-ttu-id="f8d37-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f8d37-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d37-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8d37-125">-WhatIf</span></span>
<span data-ttu-id="f8d37-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f8d37-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8d37-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f8d37-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d37-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d37-128">CommonParameters</span></span>
<span data-ttu-id="f8d37-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8d37-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8d37-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8d37-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d37-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8d37-131">INPUTS</span></span>

### <span data-ttu-id="f8d37-132">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="f8d37-132">IStorageContext</span></span>

<span data-ttu-id="f8d37-133">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f8d37-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="f8d37-134">Dizisi</span><span class="sxs-lookup"><span data-stu-id="f8d37-134">String</span></span>

<span data-ttu-id="f8d37-135">' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f8d37-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f8d37-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8d37-136">OUTPUTS</span></span>

### <span data-ttu-id="f8d37-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f8d37-137">System.Boolean</span></span>

## <span data-ttu-id="f8d37-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8d37-138">NOTES</span></span>

## <span data-ttu-id="f8d37-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8d37-139">RELATED LINKS</span></span>

[<span data-ttu-id="f8d37-140">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="f8d37-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)