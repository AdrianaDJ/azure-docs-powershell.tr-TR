---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcb08eb9e63917d072630f81a2026d961a70dd27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761712"
---
# <span data-ttu-id="9a50b-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="9a50b-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="9a50b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a50b-102">SYNOPSIS</span></span>
<span data-ttu-id="9a50b-103">Depolama tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9a50b-103">Removes a storage table.</span></span>

## <span data-ttu-id="9a50b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9a50b-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a50b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9a50b-105">DESCRIPTION</span></span>
<span data-ttu-id="9a50b-106">**Remove-AzureStorageTable** cmdlet 'ı, Azure 'daki depolama hesabından bir veya daha fazla depolama tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9a50b-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="9a50b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9a50b-107">EXAMPLES</span></span>

### <span data-ttu-id="9a50b-108">Örnek 1: tablo kaldırma</span><span class="sxs-lookup"><span data-stu-id="9a50b-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="9a50b-109">Bu komut tabloyu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9a50b-109">This command removes a table.</span></span>

### <span data-ttu-id="9a50b-110">Örnek 2: birkaç tabloyu kaldırma</span><span class="sxs-lookup"><span data-stu-id="9a50b-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="9a50b-111">Bu örnekte, desen tablosuyla eşleşen tüm tabloları almak için *Name* parametresiyle birlikte joker karakter kullanılır ve ardından tabloları kaldırmak için sonucu ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="9a50b-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="9a50b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9a50b-112">PARAMETERS</span></span>

### <span data-ttu-id="9a50b-113">-Context</span><span class="sxs-lookup"><span data-stu-id="9a50b-113">-Context</span></span>
<span data-ttu-id="9a50b-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a50b-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="9a50b-115">Bunu, New-AzureStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9a50b-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9a50b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9a50b-116">-Force</span></span>
<span data-ttu-id="9a50b-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="9a50b-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9a50b-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="9a50b-118">-Name</span></span>
<span data-ttu-id="9a50b-119">Kaldırılacak tablonun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a50b-119">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="9a50b-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9a50b-120">-PassThru</span></span>
<span data-ttu-id="9a50b-121">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="9a50b-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="9a50b-122">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="9a50b-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="9a50b-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="9a50b-123">-Confirm</span></span>
<span data-ttu-id="9a50b-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9a50b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a50b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a50b-125">-WhatIf</span></span>
<span data-ttu-id="9a50b-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9a50b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a50b-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9a50b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a50b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a50b-128">CommonParameters</span></span>
<span data-ttu-id="9a50b-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9a50b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a50b-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a50b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a50b-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9a50b-131">INPUTS</span></span>

## <span data-ttu-id="9a50b-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9a50b-132">OUTPUTS</span></span>

## <span data-ttu-id="9a50b-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9a50b-133">NOTES</span></span>

## <span data-ttu-id="9a50b-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9a50b-134">RELATED LINKS</span></span>

[<span data-ttu-id="9a50b-135">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="9a50b-135">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
