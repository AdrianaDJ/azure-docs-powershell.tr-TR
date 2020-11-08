---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: af14588394a94e771c1287081aa263a7ba8e9da1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94105021"
---
# <span data-ttu-id="71b97-101">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="71b97-101">Set-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="71b97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71b97-102">SYNOPSIS</span></span>
<span data-ttu-id="71b97-103">Data Lake Store 'da bir dosyanın veya klasörün sekizlik izin sayısını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="71b97-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="71b97-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="71b97-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Permission] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71b97-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="71b97-105">DESCRIPTION</span></span>
<span data-ttu-id="71b97-106">**Set-AzDataLakeStoreItemPermission** cmdlet 'ı, Data Lake Store 'da bir dosyanın veya klasörün sekizlik izin miktarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="71b97-106">The **Set-AzDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="71b97-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="71b97-107">EXAMPLES</span></span>

### <span data-ttu-id="71b97-108">Örnek 1: bir öğe için sekizlik izin ayarlama</span><span class="sxs-lookup"><span data-stu-id="71b97-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="71b97-109">Bu 0770 komut, yapışkan bitini temizlemeyi, dosyanın sahibi için okuma/yazma/yürütme izinlerini ayarlamak, dosyanın sahip olduğu grup için okuma/yazma/yürütme izinlerini ayarlamak ve diğer için okuma/yazma/yürütme izinlerini Temizleme</span><span class="sxs-lookup"><span data-stu-id="71b97-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="71b97-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="71b97-110">PARAMETERS</span></span>

### <span data-ttu-id="71b97-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="71b97-111">-Account</span></span>
<span data-ttu-id="71b97-112">Data Lake Store hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71b97-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="71b97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71b97-113">-DefaultProfile</span></span>
<span data-ttu-id="71b97-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="71b97-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71b97-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="71b97-115">-Path</span></span>
<span data-ttu-id="71b97-116">Kök dizinden (/) başlayarak dosya veya klasörün veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="71b97-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="71b97-117">-İzin</span><span class="sxs-lookup"><span data-stu-id="71b97-117">-Permission</span></span>
<span data-ttu-id="71b97-118">Dosya veya klasör için ayarlama izinleri (örneğin, ' 777 ')</span><span class="sxs-lookup"><span data-stu-id="71b97-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b97-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="71b97-119">-Confirm</span></span>
<span data-ttu-id="71b97-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="71b97-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71b97-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71b97-121">-WhatIf</span></span>
<span data-ttu-id="71b97-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="71b97-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71b97-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="71b97-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71b97-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b97-124">CommonParameters</span></span>
<span data-ttu-id="71b97-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="71b97-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b97-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71b97-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b97-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="71b97-127">INPUTS</span></span>

### <span data-ttu-id="71b97-128">System. String</span><span class="sxs-lookup"><span data-stu-id="71b97-128">System.String</span></span>

### <span data-ttu-id="71b97-129">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="71b97-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="71b97-130">System. Int32</span><span class="sxs-lookup"><span data-stu-id="71b97-130">System.Int32</span></span>

## <span data-ttu-id="71b97-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="71b97-131">OUTPUTS</span></span>

### <span data-ttu-id="71b97-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71b97-132">System.Boolean</span></span>

## <span data-ttu-id="71b97-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="71b97-133">NOTES</span></span>
* <span data-ttu-id="71b97-134">Diğer ad: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="71b97-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="71b97-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="71b97-135">RELATED LINKS</span></span>

[<span data-ttu-id="71b97-136">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="71b97-136">Get-AzDataLakeStoreItemPermission</span></span>](./Get-AzDataLakeStoreItemPermission.md)


