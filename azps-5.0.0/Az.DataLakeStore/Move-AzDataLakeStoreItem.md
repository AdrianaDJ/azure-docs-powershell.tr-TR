---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: e8e90b6cca2808bbf2caee69ebef5582ed0f8c5b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320538"
---
# <span data-ttu-id="2e96f-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2e96f-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="2e96f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e96f-102">SYNOPSIS</span></span>
<span data-ttu-id="2e96f-103">Data Lake Store 'da bir dosyayı veya klasörü taşıma veya yeniden adlandırmıştır.</span><span class="sxs-lookup"><span data-stu-id="2e96f-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2e96f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e96f-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e96f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e96f-105">DESCRIPTION</span></span>
<span data-ttu-id="2e96f-106">**Taþý-AzDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da bir dosyayı veya klasörü taşır veya yeniden adlandırır.</span><span class="sxs-lookup"><span data-stu-id="2e96f-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2e96f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e96f-107">EXAMPLES</span></span>

### <span data-ttu-id="2e96f-108">Örnek 1: öğeyi taşıma ve yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="2e96f-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="2e96f-109">Bu komut RenamedFile.txt için öğe File.txt yeniden adlandırır ve farklı bir klasöre taşımıştır.</span><span class="sxs-lookup"><span data-stu-id="2e96f-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="2e96f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e96f-110">PARAMETERS</span></span>

### <span data-ttu-id="2e96f-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="2e96f-111">-Account</span></span>
<span data-ttu-id="2e96f-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e96f-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e96f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e96f-113">-DefaultProfile</span></span>
<span data-ttu-id="2e96f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e96f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e96f-115">-Hedef</span><span class="sxs-lookup"><span data-stu-id="2e96f-115">-Destination</span></span>
<span data-ttu-id="2e96f-116">Kök dizinden (/) başlayarak öğenin taşınacağı Data Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e96f-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e96f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2e96f-117">-Force</span></span>
<span data-ttu-id="2e96f-118">Zaten varsa, bu işlemin hedef dosyanın üzerine yazabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="2e96f-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e96f-119">-Yol</span><span class="sxs-lookup"><span data-stu-id="2e96f-119">-Path</span></span>
<span data-ttu-id="2e96f-120">Kök dizinden (/) başlayarak taşınacak veya yeniden adlandırılacak öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e96f-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e96f-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="2e96f-121">-Confirm</span></span>
<span data-ttu-id="2e96f-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2e96f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e96f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e96f-123">-WhatIf</span></span>
<span data-ttu-id="2e96f-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2e96f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e96f-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2e96f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e96f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e96f-126">CommonParameters</span></span>
<span data-ttu-id="2e96f-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e96f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e96f-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e96f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e96f-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e96f-129">INPUTS</span></span>

### <span data-ttu-id="2e96f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2e96f-130">System.String</span></span>

### <span data-ttu-id="2e96f-131">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="2e96f-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="2e96f-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2e96f-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2e96f-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e96f-133">OUTPUTS</span></span>

### <span data-ttu-id="2e96f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2e96f-134">System.String</span></span>

## <span data-ttu-id="2e96f-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e96f-135">NOTES</span></span>

## <span data-ttu-id="2e96f-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e96f-136">RELATED LINKS</span></span>

[<span data-ttu-id="2e96f-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2e96f-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="2e96f-138">Dışarı aktarma-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2e96f-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="2e96f-139">İçeri aktarma-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2e96f-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="2e96f-140">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2e96f-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="2e96f-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2e96f-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="2e96f-142">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2e96f-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


