---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 0fd40207f72f83c68418d0184922301e137ffc1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589577"
---
# <span data-ttu-id="4df42-101">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="4df42-101">Set-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="4df42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4df42-102">SYNOPSIS</span></span>
<span data-ttu-id="4df42-103">Data Lake Store 'da bir dosya veya klasörün sahibini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4df42-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4df42-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4df42-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4df42-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4df42-105">DESCRIPTION</span></span>
<span data-ttu-id="4df42-106">**Set-AzureRmDataLakeStoreItemOwner** cmdlet 'ı, Data Lake Store 'da bir dosya veya klasörün sahibini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4df42-106">The **Set-AzureRmDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4df42-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4df42-107">EXAMPLES</span></span>

### <span data-ttu-id="4df42-108">Örnek 1: öğenin sahibini ayarlama</span><span class="sxs-lookup"><span data-stu-id="4df42-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="4df42-109">Bu komut, kök dizinin sahibini Path Tamlaştırıcı olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4df42-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="4df42-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4df42-110">PARAMETERS</span></span>

### <span data-ttu-id="4df42-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="4df42-111">-Account</span></span>
<span data-ttu-id="4df42-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4df42-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="4df42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df42-113">-DefaultProfile</span></span>
<span data-ttu-id="4df42-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4df42-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4df42-115">-ID</span><span class="sxs-lookup"><span data-stu-id="4df42-115">-Id</span></span>
<span data-ttu-id="4df42-116">Sahip olarak kullanılmak üzere AzureActive Directory kullanıcısının, grubun veya hizmet sorumlusunun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4df42-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

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

### <span data-ttu-id="4df42-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4df42-117">-PassThru</span></span>
<span data-ttu-id="4df42-118">Sonuç olarak güncelleştirilen sahibin döndürülmesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4df42-118">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="4df42-119">-Yol</span><span class="sxs-lookup"><span data-stu-id="4df42-119">-Path</span></span>
<span data-ttu-id="4df42-120">Kök dizinle (/) başlayarak değiştirilecek olan öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4df42-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="4df42-121">-Tür</span><span class="sxs-lookup"><span data-stu-id="4df42-121">-Type</span></span>
<span data-ttu-id="4df42-122">Ayarlanacak sahibin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4df42-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="4df42-123">Bu parametre için kabul edilebilir değerler: Kullanıcı ve grup.</span><span class="sxs-lookup"><span data-stu-id="4df42-123">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="4df42-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="4df42-124">-Confirm</span></span>
<span data-ttu-id="4df42-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4df42-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4df42-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4df42-126">-WhatIf</span></span>
<span data-ttu-id="4df42-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4df42-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4df42-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4df42-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4df42-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df42-129">CommonParameters</span></span>
<span data-ttu-id="4df42-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4df42-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df42-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4df42-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df42-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4df42-132">INPUTS</span></span>

### <span data-ttu-id="4df42-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4df42-133">System.String</span></span>

### <span data-ttu-id="4df42-134">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4df42-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="4df42-135">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="4df42-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="4df42-136">System. Guid</span><span class="sxs-lookup"><span data-stu-id="4df42-136">System.Guid</span></span>

### <span data-ttu-id="4df42-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4df42-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4df42-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4df42-138">OUTPUTS</span></span>

### <span data-ttu-id="4df42-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4df42-139">System.Boolean</span></span>

## <span data-ttu-id="4df42-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4df42-140">NOTES</span></span>

## <span data-ttu-id="4df42-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4df42-141">RELATED LINKS</span></span>

[<span data-ttu-id="4df42-142">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="4df42-142">Get-AzureRmDataLakeStoreItemOwner</span></span>](./Get-AzureRmDataLakeStoreItemOwner.md)


