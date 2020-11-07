---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: ba63794844420accf2e5e664a43f74b2578c780d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762676"
---
# <span data-ttu-id="04a1c-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04a1c-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="04a1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="04a1c-103">Azure 'dan depolama hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="04a1c-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04a1c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04a1c-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04a1c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="04a1c-105">DESCRIPTION</span></span>
<span data-ttu-id="04a1c-106">**Remove-AzureRmStorageAccount** cmdlet 'i Azure 'Dan bir depolama hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="04a1c-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="04a1c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04a1c-107">EXAMPLES</span></span>

### <span data-ttu-id="04a1c-108">Örnek 1: depolama hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="04a1c-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="04a1c-109">Bu komut belirtilen depolama hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="04a1c-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="04a1c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04a1c-110">PARAMETERS</span></span>

### <span data-ttu-id="04a1c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="04a1c-111">-Force</span></span>
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

### <span data-ttu-id="04a1c-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="04a1c-112">-Name</span></span>
<span data-ttu-id="04a1c-113">Kaldırılacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04a1c-113">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04a1c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04a1c-114">-ResourceGroupName</span></span>
<span data-ttu-id="04a1c-115">Kaldırılacak depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04a1c-115">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="04a1c-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="04a1c-116">-Confirm</span></span>
<span data-ttu-id="04a1c-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="04a1c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04a1c-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04a1c-118">-WhatIf</span></span>
<span data-ttu-id="04a1c-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="04a1c-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04a1c-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="04a1c-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04a1c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04a1c-121">-DefaultProfile</span></span>
<span data-ttu-id="04a1c-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="04a1c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04a1c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04a1c-123">CommonParameters</span></span>
<span data-ttu-id="04a1c-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04a1c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04a1c-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04a1c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04a1c-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04a1c-126">INPUTS</span></span>

## <span data-ttu-id="04a1c-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04a1c-127">OUTPUTS</span></span>

## <span data-ttu-id="04a1c-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04a1c-128">NOTES</span></span>

## <span data-ttu-id="04a1c-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04a1c-129">RELATED LINKS</span></span>

[<span data-ttu-id="04a1c-130">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04a1c-130">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="04a1c-131">Yeni-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04a1c-131">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="04a1c-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04a1c-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


