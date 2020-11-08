---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 9ead4b38575bc297a820bda61eb6faf0beaf80d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268562"
---
# <span data-ttu-id="fd48f-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="fd48f-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="fd48f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd48f-102">SYNOPSIS</span></span>
<span data-ttu-id="fd48f-103">Sanal makinede yedekleme uzantısı özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fd48f-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="fd48f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd48f-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd48f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd48f-105">DESCRIPTION</span></span>

## <span data-ttu-id="fd48f-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd48f-106">EXAMPLES</span></span>

### <span data-ttu-id="fd48f-107">2</span><span class="sxs-lookup"><span data-stu-id="fd48f-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="fd48f-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd48f-108">PARAMETERS</span></span>

### <span data-ttu-id="fd48f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd48f-109">-DefaultProfile</span></span>
<span data-ttu-id="fd48f-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fd48f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd48f-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="fd48f-111">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd48f-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd48f-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="fd48f-113">Etiketli</span><span class="sxs-lookup"><span data-stu-id="fd48f-113">-Tag</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd48f-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="fd48f-114">-VMName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd48f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd48f-115">CommonParameters</span></span>
<span data-ttu-id="fd48f-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd48f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd48f-117">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fd48f-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd48f-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd48f-118">INPUTS</span></span>

### <span data-ttu-id="fd48f-119">System. String</span><span class="sxs-lookup"><span data-stu-id="fd48f-119">System.String</span></span>

## <span data-ttu-id="fd48f-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd48f-120">OUTPUTS</span></span>

### <span data-ttu-id="fd48f-121">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fd48f-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="fd48f-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd48f-122">NOTES</span></span>

## <span data-ttu-id="fd48f-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd48f-123">RELATED LINKS</span></span>
