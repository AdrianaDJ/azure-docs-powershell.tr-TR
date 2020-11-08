---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: fc7c0e7ff8ef86b4a33f93e6b1286bb6e0baa00d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268303"
---
# <span data-ttu-id="7d2b7-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="7d2b7-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="7d2b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d2b7-102">SYNOPSIS</span></span>
<span data-ttu-id="7d2b7-103">Data Lake Store 'da bir dosya veya klasörün sahibini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="7d2b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d2b7-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d2b7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d2b7-105">DESCRIPTION</span></span>
<span data-ttu-id="7d2b7-106">**Set-AzDataLakeStoreItemOwner** cmdlet 'ı, Data Lake Store 'da bir dosya veya klasörün sahibini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="7d2b7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d2b7-107">EXAMPLES</span></span>

### <span data-ttu-id="7d2b7-108">Örnek 1: öğenin sahibini ayarlama</span><span class="sxs-lookup"><span data-stu-id="7d2b7-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="7d2b7-109">Bu komut, kök dizinin sahibini Path Tamlaştırıcı olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="7d2b7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d2b7-110">PARAMETERS</span></span>

### <span data-ttu-id="7d2b7-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="7d2b7-111">-Account</span></span>
<span data-ttu-id="7d2b7-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="7d2b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d2b7-113">-DefaultProfile</span></span>
<span data-ttu-id="7d2b7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d2b7-115">-ID</span><span class="sxs-lookup"><span data-stu-id="7d2b7-115">-Id</span></span>
<span data-ttu-id="7d2b7-116">Sahip olarak kullanılmak üzere AzureActive Directory kullanıcısının, grubun veya hizmet sorumlusunun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2b7-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7d2b7-117">-PassThru</span></span>
<span data-ttu-id="7d2b7-118">Sonuç olarak güncelleştirilen sahibin döndürülmesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-118">Indicates the resulting updated owner should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2b7-119">-Yol</span><span class="sxs-lookup"><span data-stu-id="7d2b7-119">-Path</span></span>
<span data-ttu-id="7d2b7-120">Kök dizinle (/) başlayarak değiştirilecek olan öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="7d2b7-121">-Tür</span><span class="sxs-lookup"><span data-stu-id="7d2b7-121">-Type</span></span>
<span data-ttu-id="7d2b7-122">Ayarlanacak sahibin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="7d2b7-123">Bu parametre için kabul edilebilir değerler: Kullanıcı ve grup.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-123">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2b7-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="7d2b7-124">-Confirm</span></span>
<span data-ttu-id="7d2b7-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d2b7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d2b7-126">-WhatIf</span></span>
<span data-ttu-id="7d2b7-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d2b7-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d2b7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d2b7-129">CommonParameters</span></span>
<span data-ttu-id="7d2b7-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d2b7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d2b7-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d2b7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d2b7-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d2b7-132">INPUTS</span></span>

### <span data-ttu-id="7d2b7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7d2b7-133">System.String</span></span>

### <span data-ttu-id="7d2b7-134">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="7d2b7-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="7d2b7-135">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="7d2b7-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="7d2b7-136">System. Guid</span><span class="sxs-lookup"><span data-stu-id="7d2b7-136">System.Guid</span></span>

### <span data-ttu-id="7d2b7-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7d2b7-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7d2b7-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d2b7-138">OUTPUTS</span></span>

### <span data-ttu-id="7d2b7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7d2b7-139">System.String</span></span>

## <span data-ttu-id="7d2b7-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d2b7-140">NOTES</span></span>

## <span data-ttu-id="7d2b7-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d2b7-141">RELATED LINKS</span></span>

[<span data-ttu-id="7d2b7-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="7d2b7-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)


