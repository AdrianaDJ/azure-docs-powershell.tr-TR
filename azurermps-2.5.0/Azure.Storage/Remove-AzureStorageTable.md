---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetable
schema: 2.0.0
ms.openlocfilehash: e33e32051c15483956d0764f5e9ddca25a083f23
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939967"
---
# <span data-ttu-id="30399-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="30399-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="30399-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30399-102">SYNOPSIS</span></span>
<span data-ttu-id="30399-103">Depolama tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="30399-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30399-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30399-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30399-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="30399-105">DESCRIPTION</span></span>
<span data-ttu-id="30399-106">**Remove-AzureStorageTable** cmdlet 'ı, Azure 'daki depolama hesabından bir veya daha fazla depolama tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="30399-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="30399-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30399-107">EXAMPLES</span></span>

### <span data-ttu-id="30399-108">Örnek 1: tablo kaldırma</span><span class="sxs-lookup"><span data-stu-id="30399-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="30399-109">Bu komut tabloyu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="30399-109">This command removes a table.</span></span>

### <span data-ttu-id="30399-110">Örnek 2: birkaç tabloyu kaldırma</span><span class="sxs-lookup"><span data-stu-id="30399-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="30399-111">Bu örnekte, desen tablosuyla eşleşen tüm tabloları almak için *Name* parametresiyle birlikte joker karakter kullanılır ve ardından tabloları kaldırmak için sonucu ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="30399-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="30399-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30399-112">PARAMETERS</span></span>

### <span data-ttu-id="30399-113">-Context</span><span class="sxs-lookup"><span data-stu-id="30399-113">-Context</span></span>
<span data-ttu-id="30399-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30399-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="30399-115">Bunu, New-AzureStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="30399-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="30399-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30399-116">-DefaultProfile</span></span>
<span data-ttu-id="30399-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="30399-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30399-118">-Force</span><span class="sxs-lookup"><span data-stu-id="30399-118">-Force</span></span>
<span data-ttu-id="30399-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="30399-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="30399-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="30399-120">-Name</span></span>
<span data-ttu-id="30399-121">Kaldırılacak tablonun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30399-121">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="30399-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="30399-122">-PassThru</span></span>
<span data-ttu-id="30399-123">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="30399-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="30399-124">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="30399-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="30399-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="30399-125">-Confirm</span></span>
<span data-ttu-id="30399-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="30399-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30399-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30399-127">-WhatIf</span></span>
<span data-ttu-id="30399-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="30399-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30399-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="30399-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30399-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30399-130">CommonParameters</span></span>
<span data-ttu-id="30399-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30399-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30399-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30399-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30399-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30399-133">INPUTS</span></span>

### <span data-ttu-id="30399-134">System. String</span><span class="sxs-lookup"><span data-stu-id="30399-134">System.String</span></span>

### <span data-ttu-id="30399-135">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="30399-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="30399-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30399-136">OUTPUTS</span></span>

### <span data-ttu-id="30399-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="30399-137">System.Boolean</span></span>

## <span data-ttu-id="30399-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30399-138">NOTES</span></span>

## <span data-ttu-id="30399-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30399-139">RELATED LINKS</span></span>

[<span data-ttu-id="30399-140">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="30399-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
