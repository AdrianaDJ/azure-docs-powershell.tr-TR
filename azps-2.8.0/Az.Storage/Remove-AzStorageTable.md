---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
ms.openlocfilehash: 77e011275a7861f54d25339fe46aad36cffe5e34
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934272"
---
# <span data-ttu-id="75d19-101">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="75d19-101">Remove-AzStorageTable</span></span>

## <span data-ttu-id="75d19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75d19-102">SYNOPSIS</span></span>
<span data-ttu-id="75d19-103">Depolama tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="75d19-103">Removes a storage table.</span></span>

## <span data-ttu-id="75d19-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75d19-104">SYNTAX</span></span>

```
Remove-AzStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75d19-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="75d19-105">DESCRIPTION</span></span>
<span data-ttu-id="75d19-106">**Remove-AzStorageTable** cmdlet 'ı, Azure 'daki depolama hesabından bir veya daha fazla depolama tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="75d19-106">The **Remove-AzStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="75d19-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75d19-107">EXAMPLES</span></span>

### <span data-ttu-id="75d19-108">Örnek 1: tablo kaldırma</span><span class="sxs-lookup"><span data-stu-id="75d19-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzStorageTable -Name "TableABC"
```

<span data-ttu-id="75d19-109">Bu komut tabloyu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="75d19-109">This command removes a table.</span></span>

### <span data-ttu-id="75d19-110">Örnek 2: birkaç tabloyu kaldırma</span><span class="sxs-lookup"><span data-stu-id="75d19-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzStorageTable table* | Remove-AzStorageTable
```

<span data-ttu-id="75d19-111">Bu örnekte, desen tablosuyla eşleşen tüm tabloları almak için *Name* parametresiyle birlikte joker karakter kullanılır ve ardından tabloları kaldırmak için sonucu ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="75d19-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="75d19-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75d19-112">PARAMETERS</span></span>

### <span data-ttu-id="75d19-113">-Context</span><span class="sxs-lookup"><span data-stu-id="75d19-113">-Context</span></span>
<span data-ttu-id="75d19-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75d19-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="75d19-115">Bunu, New-AzStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="75d19-115">You can create it by using the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75d19-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d19-116">-DefaultProfile</span></span>
<span data-ttu-id="75d19-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75d19-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d19-118">-Force</span><span class="sxs-lookup"><span data-stu-id="75d19-118">-Force</span></span>
<span data-ttu-id="75d19-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="75d19-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="75d19-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="75d19-120">-Name</span></span>
<span data-ttu-id="75d19-121">Kaldırılacak tablonun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75d19-121">Specifies the name of the table to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75d19-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="75d19-122">-PassThru</span></span>
<span data-ttu-id="75d19-123">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="75d19-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="75d19-124">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="75d19-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="75d19-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="75d19-125">-Confirm</span></span>
<span data-ttu-id="75d19-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="75d19-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75d19-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75d19-127">-WhatIf</span></span>
<span data-ttu-id="75d19-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="75d19-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75d19-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="75d19-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75d19-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d19-130">CommonParameters</span></span>
<span data-ttu-id="75d19-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75d19-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d19-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75d19-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d19-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75d19-133">INPUTS</span></span>

### <span data-ttu-id="75d19-134">System. String</span><span class="sxs-lookup"><span data-stu-id="75d19-134">System.String</span></span>

### <span data-ttu-id="75d19-135">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="75d19-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="75d19-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75d19-136">OUTPUTS</span></span>

### <span data-ttu-id="75d19-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="75d19-137">System.Boolean</span></span>

## <span data-ttu-id="75d19-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75d19-138">NOTES</span></span>

## <span data-ttu-id="75d19-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75d19-139">RELATED LINKS</span></span>

[<span data-ttu-id="75d19-140">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="75d19-140">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)
