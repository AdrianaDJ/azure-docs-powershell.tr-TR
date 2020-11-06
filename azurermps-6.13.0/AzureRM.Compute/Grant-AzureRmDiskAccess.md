---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmDiskAccess.md
ms.openlocfilehash: ae45dadd2d5af2cf81a8735ca6725ee4798dbf29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592050"
---
# <span data-ttu-id="f8d29-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f8d29-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="f8d29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8d29-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d29-103">Diske erişim verir.</span><span class="sxs-lookup"><span data-stu-id="f8d29-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8d29-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8d29-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8d29-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8d29-105">DESCRIPTION</span></span>
<span data-ttu-id="f8d29-106">**Grant-AzureRmDiskAccess** cmdlet 'ine bir diske erişim veriyor.</span><span class="sxs-lookup"><span data-stu-id="f8d29-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="f8d29-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8d29-107">EXAMPLES</span></span>

### <span data-ttu-id="f8d29-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f8d29-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="f8d29-109">60 saniye için ' ResourceGroup01 ' adındaki kaynak grubundaki ' Disk01 ' adındaki diske ' Read ' erişimi verin.</span><span class="sxs-lookup"><span data-stu-id="f8d29-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="f8d29-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8d29-110">PARAMETERS</span></span>

### <span data-ttu-id="f8d29-111">-Access</span><span class="sxs-lookup"><span data-stu-id="f8d29-111">-Access</span></span>
<span data-ttu-id="f8d29-112">Erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8d29-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d29-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="f8d29-113">-AsJob</span></span>
<span data-ttu-id="f8d29-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f8d29-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8d29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8d29-115">-DefaultProfile</span></span>
<span data-ttu-id="f8d29-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f8d29-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8d29-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="f8d29-117">-DiskName</span></span>
<span data-ttu-id="f8d29-118">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8d29-118">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d29-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="f8d29-119">-DurationInSecond</span></span>
<span data-ttu-id="f8d29-120">Erişim süresini saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8d29-120">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d29-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8d29-121">-ResourceGroupName</span></span>
<span data-ttu-id="f8d29-122">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8d29-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d29-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="f8d29-123">-Confirm</span></span>
<span data-ttu-id="f8d29-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f8d29-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d29-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8d29-125">-WhatIf</span></span>
<span data-ttu-id="f8d29-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f8d29-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8d29-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f8d29-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d29-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d29-128">CommonParameters</span></span>
<span data-ttu-id="f8d29-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8d29-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8d29-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8d29-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d29-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8d29-131">INPUTS</span></span>

### <span data-ttu-id="f8d29-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f8d29-132">System.String</span></span>

## <span data-ttu-id="f8d29-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8d29-133">OUTPUTS</span></span>

### <span data-ttu-id="f8d29-134">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="f8d29-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="f8d29-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8d29-135">NOTES</span></span>

## <span data-ttu-id="f8d29-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8d29-136">RELATED LINKS</span></span>
