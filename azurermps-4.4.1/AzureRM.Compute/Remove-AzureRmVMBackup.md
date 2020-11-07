---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMBackup.md
ms.openlocfilehash: 52abb3af83f7ee0d8724243c917e3aeb58592ac9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763389"
---
# <span data-ttu-id="c18c9-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="c18c9-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="c18c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c18c9-102">SYNOPSIS</span></span>
<span data-ttu-id="c18c9-103">Bir sanal makineden yedeklemeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c18c9-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c18c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c18c9-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c18c9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c18c9-105">DESCRIPTION</span></span>

## <span data-ttu-id="c18c9-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c18c9-106">EXAMPLES</span></span>

### <span data-ttu-id="c18c9-107">2</span><span class="sxs-lookup"><span data-stu-id="c18c9-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="c18c9-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c18c9-108">PARAMETERS</span></span>

### <span data-ttu-id="c18c9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c18c9-109">-DefaultProfile</span></span>
<span data-ttu-id="c18c9-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c18c9-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c18c9-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c18c9-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c18c9-112">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c18c9-112">-Tag</span></span>
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

### <span data-ttu-id="c18c9-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="c18c9-113">-VMName</span></span>
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

### <span data-ttu-id="c18c9-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c18c9-114">CommonParameters</span></span>
<span data-ttu-id="c18c9-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c18c9-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c18c9-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c18c9-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c18c9-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c18c9-117">INPUTS</span></span>

## <span data-ttu-id="c18c9-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c18c9-118">OUTPUTS</span></span>

## <span data-ttu-id="c18c9-119">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c18c9-119">NOTES</span></span>

## <span data-ttu-id="c18c9-120">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c18c9-120">RELATED LINKS</span></span>

