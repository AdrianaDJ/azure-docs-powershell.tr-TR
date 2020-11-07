---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: fc71ec338303876a2cff44a07632e9fae5d3d2d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765181"
---
# <span data-ttu-id="59394-101">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="59394-101">Set-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="59394-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59394-102">SYNOPSIS</span></span>
<span data-ttu-id="59394-103">Data Lake Store 'da bir dosya veya klasörün sahibini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="59394-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59394-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59394-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59394-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="59394-105">DESCRIPTION</span></span>
<span data-ttu-id="59394-106">**Set-AzureRmDataLakeStoreItemOwner** cmdlet 'ı, Data Lake Store 'da bir dosya veya klasörün sahibini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="59394-106">The **Set-AzureRmDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="59394-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59394-107">EXAMPLES</span></span>

### <span data-ttu-id="59394-108">Örnek 1: öğenin sahibini ayarlama</span><span class="sxs-lookup"><span data-stu-id="59394-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="59394-109">Bu komut, kök dizinin sahibini Path Tamlaştırıcı olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="59394-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="59394-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59394-110">PARAMETERS</span></span>

### <span data-ttu-id="59394-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="59394-111">-Account</span></span>
<span data-ttu-id="59394-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59394-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="59394-113">-ID</span><span class="sxs-lookup"><span data-stu-id="59394-113">-Id</span></span>
<span data-ttu-id="59394-114">Sahip olarak kullanılmak üzere AzureActive Directory kullanıcısının, grubun veya hizmet sorumlusunun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="59394-114">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

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

### <span data-ttu-id="59394-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="59394-115">-PassThru</span></span>
<span data-ttu-id="59394-116">Sonuç olarak güncelleştirilen sahibin döndürülmesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59394-116">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="59394-117">-Yol</span><span class="sxs-lookup"><span data-stu-id="59394-117">-Path</span></span>
<span data-ttu-id="59394-118">Kök dizinle (/) başlayarak değiştirilecek olan öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="59394-118">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="59394-119">-Tür</span><span class="sxs-lookup"><span data-stu-id="59394-119">-Type</span></span>
<span data-ttu-id="59394-120">Ayarlanacak sahibin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="59394-120">Specifies the type of owner to set.</span></span>
<span data-ttu-id="59394-121">Bu parametre için kabul edilebilir değerler: Kullanıcı ve grup.</span><span class="sxs-lookup"><span data-stu-id="59394-121">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="59394-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="59394-122">-Confirm</span></span>
<span data-ttu-id="59394-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59394-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59394-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59394-124">-WhatIf</span></span>
<span data-ttu-id="59394-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59394-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59394-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="59394-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59394-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59394-127">-DefaultProfile</span></span>
<span data-ttu-id="59394-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59394-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59394-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59394-129">CommonParameters</span></span>
<span data-ttu-id="59394-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59394-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59394-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59394-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59394-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59394-132">INPUTS</span></span>

## <span data-ttu-id="59394-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59394-133">OUTPUTS</span></span>

### <span data-ttu-id="59394-134">dizisi</span><span class="sxs-lookup"><span data-stu-id="59394-134">string</span></span>
<span data-ttu-id="59394-135">Geçiş belirtildiyse, güncelleştirilmiş sahibi döndürür.</span><span class="sxs-lookup"><span data-stu-id="59394-135">If PassThru is specified, returns the updated owner.</span></span>

## <span data-ttu-id="59394-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59394-136">NOTES</span></span>

## <span data-ttu-id="59394-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59394-137">RELATED LINKS</span></span>

[<span data-ttu-id="59394-138">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="59394-138">Get-AzureRmDataLakeStoreItemOwner</span></span>](./Get-AzureRmDataLakeStoreItemOwner.md)


