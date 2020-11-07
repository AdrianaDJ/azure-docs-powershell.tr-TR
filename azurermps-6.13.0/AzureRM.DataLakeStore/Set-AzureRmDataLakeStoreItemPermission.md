---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 9a0b5f54b4bdbdee80cdade05716ff5508324b91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762486"
---
# <span data-ttu-id="66673-101">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="66673-101">Set-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="66673-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66673-102">SYNOPSIS</span></span>
<span data-ttu-id="66673-103">Data Lake Store 'da bir dosyanın veya klasörün sekizlik izin sayısını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="66673-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66673-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66673-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Permission] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66673-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="66673-105">DESCRIPTION</span></span>
<span data-ttu-id="66673-106">**Set-AzureRmDataLakeStoreItemPermission** cmdlet 'ı, Data Lake Store 'da bir dosyanın veya klasörün sekizlik izin miktarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="66673-106">The **Set-AzureRmDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="66673-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66673-107">EXAMPLES</span></span>

### <span data-ttu-id="66673-108">Örnek 1: bir öğe için sekizlik izin ayarlama</span><span class="sxs-lookup"><span data-stu-id="66673-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="66673-109">Bu 0770 komut, yapışkan bitini temizlemeyi, dosyanın sahibi için okuma/yazma/yürütme izinlerini ayarlamak, dosyanın sahip olduğu grup için okuma/yazma/yürütme izinlerini ayarlamak ve diğer için okuma/yazma/yürütme izinlerini Temizleme</span><span class="sxs-lookup"><span data-stu-id="66673-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="66673-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66673-110">PARAMETERS</span></span>

### <span data-ttu-id="66673-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="66673-111">-Account</span></span>
<span data-ttu-id="66673-112">Data Lake Store hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="66673-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="66673-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66673-113">-DefaultProfile</span></span>
<span data-ttu-id="66673-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66673-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66673-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="66673-115">-Path</span></span>
<span data-ttu-id="66673-116">Kök dizinden (/) başlayarak dosya veya klasörün veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="66673-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="66673-117">-İzin</span><span class="sxs-lookup"><span data-stu-id="66673-117">-Permission</span></span>
<span data-ttu-id="66673-118">Dosya veya klasör için ayarlama izinleri (örneğin, ' 777 ')</span><span class="sxs-lookup"><span data-stu-id="66673-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

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

### <span data-ttu-id="66673-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="66673-119">-Confirm</span></span>
<span data-ttu-id="66673-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="66673-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66673-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66673-121">-WhatIf</span></span>
<span data-ttu-id="66673-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="66673-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66673-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="66673-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66673-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66673-124">CommonParameters</span></span>
<span data-ttu-id="66673-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66673-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66673-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66673-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66673-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66673-127">INPUTS</span></span>

### <span data-ttu-id="66673-128">System. String</span><span class="sxs-lookup"><span data-stu-id="66673-128">System.String</span></span>

### <span data-ttu-id="66673-129">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="66673-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="66673-130">System. Int32</span><span class="sxs-lookup"><span data-stu-id="66673-130">System.Int32</span></span>

## <span data-ttu-id="66673-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66673-131">OUTPUTS</span></span>

### <span data-ttu-id="66673-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66673-132">System.Boolean</span></span>

## <span data-ttu-id="66673-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66673-133">NOTES</span></span>
* <span data-ttu-id="66673-134">Diğer ad: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="66673-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="66673-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66673-135">RELATED LINKS</span></span>

[<span data-ttu-id="66673-136">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="66673-136">Get-AzureRmDataLakeStoreItemPermission</span></span>](./Get-AzureRmDataLakeStoreItemPermission.md)

