---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Sync-AzureRmMediaServiceStorageKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Sync-AzureRmMediaServiceStorageKeys.md
ms.openlocfilehash: 71112bf54f4de8e0c7e4fd1ecfd296eff45ac868
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593544"
---
# <span data-ttu-id="0db3a-101">Sync-AzureRmMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="0db3a-101">Sync-AzureRmMediaServiceStorageKeys</span></span>

## <span data-ttu-id="0db3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0db3a-102">SYNOPSIS</span></span>
<span data-ttu-id="0db3a-103">Medya hizmetiyle ilişkili bir depolama hesabı için depolama hesabı anahtarlarını eşitler.</span><span class="sxs-lookup"><span data-stu-id="0db3a-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0db3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0db3a-104">SYNTAX</span></span>

```
Sync-AzureRmMediaServiceStorageKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0db3a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0db3a-105">DESCRIPTION</span></span>
<span data-ttu-id="0db3a-106">**Sync-AzureRmMediaServiceStorageKeys** cmdlet 'i, medya hizmetiyle ilişkili bir depolama hesabının depolama hesabı anahtarlarını eşitler.</span><span class="sxs-lookup"><span data-stu-id="0db3a-106">The **Sync-AzureRmMediaServiceStorageKeys** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="0db3a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0db3a-107">EXAMPLES</span></span>

### <span data-ttu-id="0db3a-108">Örnek 1: medya hizmetiyle ilişkili bir depolama hesabı için depolama hesabı anahtarlarını eşitleme</span><span class="sxs-lookup"><span data-stu-id="0db3a-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzureRmStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzureRmMediaServiceStorageKeys -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="0db3a-109">İlk komut, Storage135 adındaki depolama hesabını almak için Get-AzureRmStorageAccount cmdlet 'ini kullanır ve sonucu $StorageAccount adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="0db3a-109">The first command uses the Get-AzureRmStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>

<span data-ttu-id="0db3a-110">İkinci komut, $StorageAccount değişkeninde bulunan **ID** özelliğini kullanarak MediaService001 adındaki medya hizmeti için depolama hesabı anahtarlarını eşitler.</span><span class="sxs-lookup"><span data-stu-id="0db3a-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="0db3a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0db3a-111">PARAMETERS</span></span>

### <span data-ttu-id="0db3a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0db3a-112">-AccountName</span></span>
<span data-ttu-id="0db3a-113">Bu cmdlet 'in eşitlenei ortam hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0db3a-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db3a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0db3a-114">-ResourceGroupName</span></span>
<span data-ttu-id="0db3a-115">Medya hizmeti 'ni içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0db3a-115">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db3a-116">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="0db3a-116">-StorageAccountId</span></span>
<span data-ttu-id="0db3a-117">Medya Hizmeti hesabıyla ilişkili depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0db3a-117">Specifies the storage account ID associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db3a-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="0db3a-118">-Confirm</span></span>
<span data-ttu-id="0db3a-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0db3a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0db3a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0db3a-120">-WhatIf</span></span>
<span data-ttu-id="0db3a-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0db3a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0db3a-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0db3a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0db3a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db3a-123">-DefaultProfile</span></span>
<span data-ttu-id="0db3a-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0db3a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0db3a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db3a-125">CommonParameters</span></span>
<span data-ttu-id="0db3a-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0db3a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db3a-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0db3a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db3a-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0db3a-128">INPUTS</span></span>

## <span data-ttu-id="0db3a-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0db3a-129">OUTPUTS</span></span>

### <span data-ttu-id="0db3a-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0db3a-130">System.Boolean</span></span>

## <span data-ttu-id="0db3a-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0db3a-131">NOTES</span></span>

## <span data-ttu-id="0db3a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0db3a-132">RELATED LINKS</span></span>

