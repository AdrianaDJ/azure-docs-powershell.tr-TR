---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 1f4844ae499f68031af89e801023c849577794f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917244"
---
# <span data-ttu-id="d4f61-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="d4f61-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="d4f61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4f61-102">SYNOPSIS</span></span>
<span data-ttu-id="d4f61-103">Sanal makinede yedekleme uzantısı özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d4f61-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="d4f61-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4f61-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4f61-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4f61-105">DESCRIPTION</span></span>

## <span data-ttu-id="d4f61-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4f61-106">EXAMPLES</span></span>

### <span data-ttu-id="d4f61-107">2</span><span class="sxs-lookup"><span data-stu-id="d4f61-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="d4f61-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4f61-108">PARAMETERS</span></span>

### <span data-ttu-id="d4f61-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4f61-109">-DefaultProfile</span></span>
<span data-ttu-id="d4f61-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d4f61-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4f61-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="d4f61-111">-Name</span></span>
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

### <span data-ttu-id="d4f61-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4f61-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d4f61-113">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d4f61-113">-Tag</span></span>
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

### <span data-ttu-id="d4f61-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="d4f61-114">-VMName</span></span>
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

### <span data-ttu-id="d4f61-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4f61-115">CommonParameters</span></span>
<span data-ttu-id="d4f61-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4f61-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4f61-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4f61-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4f61-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4f61-118">INPUTS</span></span>

### <span data-ttu-id="d4f61-119">System. String</span><span class="sxs-lookup"><span data-stu-id="d4f61-119">System.String</span></span>

## <span data-ttu-id="d4f61-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4f61-120">OUTPUTS</span></span>

### <span data-ttu-id="d4f61-121">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d4f61-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d4f61-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4f61-122">NOTES</span></span>

## <span data-ttu-id="d4f61-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4f61-123">RELATED LINKS</span></span>
